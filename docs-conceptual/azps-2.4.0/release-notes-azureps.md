---
ms.openlocfilehash: f357a17f698d68c1a29dcb78f83671973fd6ecad
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863732"
---
## <a name="240---july-2019"></a><span data-ttu-id="cb151-101">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="cb151-101">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb151-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-102">Az.Accounts</span></span>
* <span data-ttu-id="cb151-103">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-103">Add support for profile cmdlets</span></span>
* <span data-ttu-id="cb151-104">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-104">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="cb151-105">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-105">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cb151-106">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cb151-106">Az.Advisor</span></span>
* <span data-ttu-id="cb151-107">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="cb151-107">GA release of Az.Advisor</span></span>
* <span data-ttu-id="cb151-108">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="cb151-108">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cb151-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb151-109">Az.ApiManagement</span></span>
* <span data-ttu-id="cb151-110">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-110">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="cb151-111">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cb151-111">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="cb151-112">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-112">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="cb151-113">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-113">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="cb151-114">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-114">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="cb151-115">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb151-115">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="cb151-116">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-116">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb151-117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb151-117">Az.Automation</span></span>
* <span data-ttu-id="cb151-118">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="cb151-118">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-119">Az.Compute</span></span>
* <span data-ttu-id="cb151-120">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="cb151-120">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb151-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb151-121">Az.DataFactory</span></span>
* <span data-ttu-id="cb151-122">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="cb151-122">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb151-123">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb151-123">Az.EventGrid</span></span>
* <span data-ttu-id="cb151-124">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="cb151-124">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb151-125">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb151-125">Az.IotHub</span></span>
* <span data-ttu-id="cb151-126">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="cb151-126">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-127">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-127">Az.Network</span></span>
* <span data-ttu-id="cb151-128">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="cb151-128">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="cb151-129">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="cb151-129">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb151-130">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-130">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb151-131">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="cb151-131">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="cb151-132">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="cb151-132">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb151-133">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-133">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb151-134">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="cb151-134">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-135">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-135">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb151-136">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="cb151-136">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-137">Az.Resources</span></span>
    - <span data-ttu-id="cb151-138">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="cb151-138">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="cb151-139">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="cb151-139">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="cb151-140">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="cb151-140">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="cb151-141">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="cb151-141">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb151-142">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb151-142">Az.ServiceBus</span></span>
* <span data-ttu-id="cb151-143">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="cb151-143">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-144">Az.Sql</span></span>
* <span data-ttu-id="cb151-145">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="cb151-145">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="cb151-146">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="cb151-146">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="cb151-147">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb151-147">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb151-148">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb151-148">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb151-149">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cb151-149">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cb151-150">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb151-150">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cb151-151">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb151-151">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cb151-152">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cb151-152">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="cb151-153">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="cb151-153">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb151-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-154">Az.Storage</span></span>
* <span data-ttu-id="cb151-155">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="cb151-155">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="cb151-156">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb151-156">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="cb151-157">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="cb151-157">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="cb151-158">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="cb151-158">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="cb151-159">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="cb151-159">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="cb151-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb151-160">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cb151-161">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb151-161">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cb151-162">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="cb151-162">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="cb151-163">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb151-163">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="cb151-164">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cb151-164">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cb151-165">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cb151-165">Az.StorageSync</span></span>
* <span data-ttu-id="cb151-166">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="cb151-166">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="cb151-167">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="cb151-167">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb151-168">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-168">Az.Accounts</span></span>
* <span data-ttu-id="cb151-169">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cb151-169">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="cb151-170">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="cb151-170">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="cb151-171">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="cb151-171">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="cb151-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cb151-172">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="cb151-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="cb151-173">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-174">Az.Compute</span></span>
* <span data-ttu-id="cb151-175">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="cb151-175">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="cb151-176">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="cb151-176">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="cb151-177">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cb151-177">Az.Dns</span></span>
* <span data-ttu-id="cb151-178">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="cb151-178">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb151-179">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb151-179">Az.EventGrid</span></span>
* <span data-ttu-id="cb151-180">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cb151-180">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="cb151-181">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cb151-181">New cmdlets:</span></span>
    - <span data-ttu-id="cb151-182">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb151-182">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb151-183">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="cb151-183">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb151-184">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb151-184">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb151-185">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="cb151-185">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="cb151-186">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cb151-186">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cb151-187">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="cb151-187">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb151-188">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cb151-188">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cb151-189">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="cb151-189">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cb151-190">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cb151-190">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cb151-191">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="cb151-191">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="cb151-192">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="cb151-192">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cb151-193">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="cb151-193">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="cb151-194">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cb151-194">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="cb151-195">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="cb151-195">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="cb151-196">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="cb151-196">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cb151-197">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="cb151-197">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="cb151-198">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cb151-198">Updated cmdlets:</span></span>
    - <span data-ttu-id="cb151-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="cb151-199">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="cb151-200">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="cb151-200">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cb151-201">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="cb151-201">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cb151-202">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="cb151-202">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="cb151-203">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="cb151-203">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="cb151-204">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="cb151-204">Event subscription expiration date,</span></span>
            - <span data-ttu-id="cb151-205">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="cb151-205">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="cb151-206">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="cb151-206">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="cb151-207">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="cb151-207">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="cb151-208">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="cb151-208">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="cb151-209">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="cb151-209">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="cb151-210">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cb151-210">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="cb151-211">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="cb151-211">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="cb151-212">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="cb151-212">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb151-213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb151-213">Az.FrontDoor</span></span>
* <span data-ttu-id="cb151-214">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="cb151-214">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="cb151-215">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="cb151-215">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="cb151-216">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cb151-216">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="cb151-217">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="cb151-217">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-218">Az.Network</span></span>
* <span data-ttu-id="cb151-219">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-219">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="cb151-220">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-220">New cmdlets</span></span>
        - <span data-ttu-id="cb151-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="cb151-221">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="cb151-222">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cb151-222">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="cb151-223">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-223">New cmdlets</span></span> 
        - <span data-ttu-id="cb151-224">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cb151-224">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="cb151-225">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb151-225">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="cb151-226">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-226">New cmdlets</span></span> 
        - <span data-ttu-id="cb151-227">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb151-227">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="cb151-228">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb151-228">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb151-229">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cb151-229">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cb151-230">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb151-230">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="cb151-231">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cb151-231">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cb151-232">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb151-232">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="cb151-233">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-233">New cmdlets</span></span>
        - <span data-ttu-id="cb151-234">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb151-234">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb151-235">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb151-235">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb151-236">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb151-236">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cb151-237">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="cb151-237">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="cb151-238">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="cb151-238">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="cb151-239">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="cb151-239">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="cb151-240">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="cb151-240">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="cb151-241">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="cb151-241">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="cb151-242">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="cb151-242">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="cb151-243">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="cb151-243">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="cb151-244">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="cb151-244">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="cb151-245">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="cb151-245">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="cb151-246">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-246">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="cb151-247">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="cb151-247">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="cb151-248">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="cb151-248">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="cb151-249">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-249">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="cb151-250">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="cb151-250">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="cb151-251">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-251">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="cb151-252">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cb151-252">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cb151-253">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="cb151-253">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="cb151-254">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="cb151-254">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="cb151-255">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="cb151-255">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="cb151-256">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="cb151-256">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="cb151-257">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="cb151-257">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="cb151-258">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="cb151-258">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cb151-259">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="cb151-259">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cb151-260">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="cb151-260">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb151-261">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-261">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb151-262">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="cb151-262">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-263">Az.Resources</span></span>
* <span data-ttu-id="cb151-264">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="cb151-264">Support for additional Template Export options</span></span>
    - <span data-ttu-id="cb151-265">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cb151-265">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cb151-266">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cb151-266">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cb151-267">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="cb151-267">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb151-268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb151-268">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb151-269">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-269">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-270">Az.Sql</span></span>
* <span data-ttu-id="cb151-271">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="cb151-271">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="cb151-272">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="cb151-272">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="cb151-273">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="cb151-273">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="cb151-274">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb151-274">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb151-275">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb151-275">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb151-276">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cb151-276">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cb151-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cb151-277">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="cb151-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cb151-278">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb151-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-279">Az.Storage</span></span>
* <span data-ttu-id="cb151-280">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="cb151-280">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="cb151-281">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb151-281">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb151-282">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="cb151-282">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="cb151-283">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cb151-283">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-284">Az.Websites</span></span>
* <span data-ttu-id="cb151-285">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="cb151-285">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="cb151-286">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="cb151-286">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="cb151-287">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="cb151-287">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="cb151-288">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb151-288">Az.Cdn</span></span>
* <span data-ttu-id="cb151-289">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="cb151-289">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-290">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-290">Az.Compute</span></span>
* <span data-ttu-id="cb151-291">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="cb151-291">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="cb151-292">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb151-292">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb151-293">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb151-293">Az.EventHub</span></span>
* <span data-ttu-id="cb151-294">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="cb151-294">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="cb151-295">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb151-295">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-296">Az.Network</span></span>
* <span data-ttu-id="cb151-297">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="cb151-297">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="cb151-298">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="cb151-298">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb151-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb151-300">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="cb151-300">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-301">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-301">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb151-302">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="cb151-302">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb151-303">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb151-303">Az.ServiceBus</span></span>
* <span data-ttu-id="cb151-304">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb151-304">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb151-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb151-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb151-306">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="cb151-306">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="cb151-307">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="cb151-307">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-308">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-308">Az.Sql</span></span>
* <span data-ttu-id="cb151-309">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="cb151-309">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="cb151-310">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-310">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cb151-311">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="cb151-311">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="cb151-312">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="cb151-312">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-313">Az.Websites</span></span>
* <span data-ttu-id="cb151-314">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-314">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="cb151-315">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="cb151-315">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cb151-316">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb151-316">Az.ApiManagement</span></span>
* <span data-ttu-id="cb151-317">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="cb151-317">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="cb151-318">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="cb151-318">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="cb151-319">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="cb151-319">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="cb151-320">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="cb151-320">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="cb151-321">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="cb151-321">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="cb151-322">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="cb151-322">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="cb151-323">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="cb151-323">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="cb151-324">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="cb151-324">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="cb151-325">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="cb151-325">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="cb151-326">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="cb151-326">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="cb151-327">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="cb151-327">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="cb151-328">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="cb151-328">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="cb151-329">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="cb151-329">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="cb151-330">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="cb151-330">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="cb151-331">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="cb151-331">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="cb151-332">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="cb151-332">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="cb151-333">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="cb151-333">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="cb151-334">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="cb151-334">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="cb151-335">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="cb151-335">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="cb151-336">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="cb151-336">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="cb151-337">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="cb151-337">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="cb151-338">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="cb151-338">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="cb151-339">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="cb151-339">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="cb151-340">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="cb151-340">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="cb151-341">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-341">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="cb151-342">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-342">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="cb151-343">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="cb151-343">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="cb151-344">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="cb151-344">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="cb151-345">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="cb151-345">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="cb151-346">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="cb151-346">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="cb151-347">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cb151-347">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="cb151-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="cb151-348">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="cb151-349">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="cb151-349">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="cb151-350">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb151-350">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cb151-351">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="cb151-351">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="cb151-352">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="cb151-352">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="cb151-353">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="cb151-353">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="cb151-354">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="cb151-354">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="cb151-355">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="cb151-355">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="cb151-356">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb151-356">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="cb151-357">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="cb151-357">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cb151-358">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="cb151-358">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cb151-359">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="cb151-359">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="cb151-360">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="cb151-360">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="cb151-361">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cb151-361">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cb151-362">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="cb151-362">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cb151-363">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="cb151-363">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="cb151-364">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="cb151-364">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="cb151-365">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="cb151-365">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="cb151-366">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="cb151-366">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="cb151-367">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="cb151-367">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="cb151-368">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="cb151-368">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="cb151-369">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="cb151-369">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="cb151-370">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="cb151-370">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="cb151-371">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="cb151-371">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="cb151-372">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="cb151-372">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="cb151-373">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cb151-373">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cb151-374">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="cb151-374">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cb151-375">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="cb151-375">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cb151-376">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="cb151-376">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cb151-377">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cb151-377">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cb151-378">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="cb151-378">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cb151-379">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="cb151-379">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cb151-380">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="cb151-380">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cb151-381">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="cb151-381">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="cb151-382">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="cb151-382">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="cb151-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="cb151-383">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="cb151-384">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="cb151-384">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="cb151-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="cb151-385">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="cb151-386">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="cb151-386">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="cb151-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="cb151-387">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="cb151-388">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="cb151-388">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="cb151-389">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="cb151-389">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="cb151-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="cb151-390">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="cb151-391">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="cb151-391">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="cb151-392">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="cb151-392">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="cb151-393">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="cb151-393">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb151-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb151-394">Az.Automation</span></span>
* <span data-ttu-id="cb151-395">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="cb151-395">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="cb151-396">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-396">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="cb151-397">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-397">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="cb151-398">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="cb151-398">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="cb151-399">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-399">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="cb151-400">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="cb151-400">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="cb151-401">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="cb151-401">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-402">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-402">Az.Compute</span></span>
* <span data-ttu-id="cb151-403">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb151-403">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="cb151-404">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="cb151-404">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb151-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb151-406">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="cb151-406">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb151-407">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb151-407">Az.Monitor</span></span>
* <span data-ttu-id="cb151-408">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="cb151-408">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-409">Az.Network</span></span>
* <span data-ttu-id="cb151-410">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="cb151-410">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="cb151-411">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cb151-411">Updated cmdlet:</span></span>
        - <span data-ttu-id="cb151-412">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb151-412">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="cb151-413">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="cb151-413">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-414">Az.Resources</span></span>
* <span data-ttu-id="cb151-415">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="cb151-415">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-416">Az.Sql</span></span>
* <span data-ttu-id="cb151-417">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="cb151-417">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="cb151-418">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="cb151-418">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb151-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-419">Az.Accounts</span></span>
* <span data-ttu-id="cb151-420">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="cb151-420">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb151-421">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb151-421">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb151-422">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="cb151-422">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="cb151-423">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb151-423">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-424">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-424">Az.Compute</span></span>
* <span data-ttu-id="cb151-425">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="cb151-425">Proximity placement group feature.</span></span>
    - <span data-ttu-id="cb151-426">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cb151-426">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="cb151-427">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cb151-427">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="cb151-428">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="cb151-428">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="cb151-429">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="cb151-429">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="cb151-430">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb151-430">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="cb151-431">重大變更</span><span class="sxs-lookup"><span data-stu-id="cb151-431">Breaking changes</span></span>
    - <span data-ttu-id="cb151-432">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="cb151-432">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="cb151-433">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="cb151-433">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cb151-434">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cb151-434">Az.DeploymentManager</span></span>
* <span data-ttu-id="cb151-435">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-435">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="cb151-436">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cb151-436">Az.Dns</span></span>
* <span data-ttu-id="cb151-437">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="cb151-437">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="cb151-438">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="cb151-438">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="cb151-439">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="cb151-439">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cb151-440">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb151-440">Az.FrontDoor</span></span>
* <span data-ttu-id="cb151-441">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-441">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="cb151-442">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="cb151-442">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="cb151-443">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb151-443">Az.HDInsight</span></span>
* <span data-ttu-id="cb151-444">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cb151-444">Removed two cmdlets:</span></span>
    - <span data-ttu-id="cb151-445">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb151-445">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="cb151-446">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb151-446">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cb151-447">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cb151-447">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cb151-448">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="cb151-448">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="cb151-449">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb151-449">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="cb151-450">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="cb151-450">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb151-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb151-451">Az.Monitor</span></span>
* <span data-ttu-id="cb151-452">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="cb151-452">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="cb151-453">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="cb151-453">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="cb151-454">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="cb151-454">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="cb151-455">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cb151-455">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="cb151-456">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cb151-456">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="cb151-457">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cb151-457">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="cb151-458">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cb151-458">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="cb151-459">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb151-459">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb151-460">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb151-460">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb151-461">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb151-461">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb151-462">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb151-462">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb151-463">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cb151-463">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cb151-464">[更多](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="cb151-464">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="cb151-465">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-465">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-466">Az.Network</span></span>
* <span data-ttu-id="cb151-467">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-467">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="cb151-468">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-468">New cmdlets</span></span>
        - <span data-ttu-id="cb151-469">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb151-469">New-AzNatGateway</span></span>
        - <span data-ttu-id="cb151-470">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb151-470">Get-AzNatGateway</span></span>
        - <span data-ttu-id="cb151-471">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb151-471">Set-AzNatGateway</span></span>
        - <span data-ttu-id="cb151-472">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cb151-472">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="cb151-473">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-473">Updated cmdlets</span></span>
        - <span data-ttu-id="cb151-474">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cb151-474">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="cb151-475">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cb151-475">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="cb151-476">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="cb151-476">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="cb151-477">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="cb151-477">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="cb151-478">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="cb151-478">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb151-479">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-479">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb151-480">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cb151-480">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="cb151-481">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="cb151-481">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="cb151-482">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="cb151-482">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-483">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-483">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb151-484">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="cb151-484">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="cb151-485">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="cb151-485">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="cb151-486">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="cb151-486">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="cb151-487">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="cb151-487">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="cb151-488">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="cb151-488">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="cb151-489">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="cb151-489">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="cb151-490">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb151-490">Az.Relay</span></span>
* <span data-ttu-id="cb151-491">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="cb151-491">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb151-492">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb151-492">Az.ServiceBus</span></span>
* <span data-ttu-id="cb151-493">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-493">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb151-494">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-494">Az.Storage</span></span>
* <span data-ttu-id="cb151-495">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="cb151-495">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="cb151-496">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="cb151-496">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="cb151-497">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="cb151-497">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="cb151-498">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb151-498">New-AzStorageAccount</span></span>
* <span data-ttu-id="cb151-499">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="cb151-499">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="cb151-500">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb151-500">New-AzStorageAccount</span></span>
    - <span data-ttu-id="cb151-501">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb151-501">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="cb151-502">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb151-502">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-503">Az.Websites</span></span>
* <span data-ttu-id="cb151-504">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="cb151-504">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="cb151-505">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="cb151-505">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="cb151-506">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="cb151-506">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb151-507">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cb151-507">Highlights since the last major release</span></span>
* <span data-ttu-id="cb151-508">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="cb151-508">General availability of `Az` module</span></span>
* <span data-ttu-id="cb151-509">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb151-509">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb151-510">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb151-510">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb151-511">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cb151-511">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb151-512">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="cb151-512">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb151-513">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-513">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb151-514">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-514">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb151-515">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-515">Az.Accounts</span></span>
* <span data-ttu-id="cb151-516">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="cb151-516">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cb151-517">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb151-517">Az.Batch</span></span>
* <span data-ttu-id="cb151-518">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-518">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb151-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb151-519">Az.Cdn</span></span>
* <span data-ttu-id="cb151-520">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb151-521">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb151-521">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb151-522">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-522">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-523">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-523">Az.Compute</span></span>
* <span data-ttu-id="cb151-524">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="cb151-524">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cb151-525">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb151-526">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb151-526">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb151-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb151-527">Az.DataFactory</span></span>
* <span data-ttu-id="cb151-528">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="cb151-528">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb151-529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-529">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb151-530">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-530">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb151-531">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb151-531">Az.EventGrid</span></span>
* <span data-ttu-id="cb151-532">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb151-532">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb151-533">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb151-533">Az.EventHub</span></span>
* <span data-ttu-id="cb151-534">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-534">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="cb151-535">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cb151-535">Az.HDInsight</span></span>
* <span data-ttu-id="cb151-536">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-536">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb151-537">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb151-537">Az.IotHub</span></span>
* <span data-ttu-id="cb151-538">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-538">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb151-539">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb151-539">Az.KeyVault</span></span>
* <span data-ttu-id="cb151-540">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-540">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb151-541">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb151-541">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cb151-542">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb151-542">Az.MachineLearning</span></span>
* <span data-ttu-id="cb151-543">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cb151-544">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb151-544">Az.Media</span></span>
* <span data-ttu-id="cb151-545">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb151-546">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb151-546">Az.Monitor</span></span>
  * <span data-ttu-id="cb151-547">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-547">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cb151-548">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cb151-548">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cb151-549">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cb151-549">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cb151-550">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb151-550">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb151-551">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb151-551">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cb151-552">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cb151-552">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cb151-553">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="cb151-553">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-554">Az.Network</span></span>
* <span data-ttu-id="cb151-555">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-555">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb151-556">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb151-556">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cb151-557">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cb151-557">Az.NotificationHubs</span></span>
* <span data-ttu-id="cb151-558">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-558">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb151-559">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-559">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb151-560">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-560">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cb151-561">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cb151-561">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cb151-562">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-563">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-563">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb151-564">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-564">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb151-565">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="cb151-565">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cb151-566">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="cb151-566">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cb151-567">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="cb151-567">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb151-568">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb151-568">Az.RedisCache</span></span>
* <span data-ttu-id="cb151-569">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-570">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-570">Az.Resources</span></span>
* <span data-ttu-id="cb151-571">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb151-571">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-572">Az.Sql</span></span>
* <span data-ttu-id="cb151-573">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="cb151-573">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cb151-574">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-574">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb151-575">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="cb151-575">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cb151-576">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="cb151-576">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cb151-577">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="cb151-577">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cb151-578">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="cb151-578">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cb151-579">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="cb151-579">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-580">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-580">Az.Websites</span></span>
* <span data-ttu-id="cb151-581">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="cb151-581">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cb151-582">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-582">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cb151-583">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="cb151-583">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cb151-584">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="cb151-584">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cb151-585">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="cb151-585">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb151-586">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cb151-586">Highlights since the last major release</span></span>
* <span data-ttu-id="cb151-587">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="cb151-587">General availability of `Az` module</span></span>
* <span data-ttu-id="cb151-588">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb151-588">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb151-589">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb151-589">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb151-590">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cb151-590">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb151-591">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="cb151-591">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb151-592">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-592">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb151-593">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-593">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cb151-594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-594">Az.Accounts</span></span>
* <span data-ttu-id="cb151-595">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="cb151-595">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb151-596">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb151-596">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb151-597">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="cb151-597">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cb151-598">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="cb151-598">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb151-599">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb151-599">Az.Automation</span></span>
* <span data-ttu-id="cb151-600">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="cb151-600">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cb151-601">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="cb151-601">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cb151-602">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="cb151-602">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-603">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-603">Az.Compute</span></span>
* <span data-ttu-id="cb151-604">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cb151-604">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cb151-605">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="cb151-605">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="cb151-606">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb151-606">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb151-607">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="cb151-607">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb151-608">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb151-608">Az.DataFactory</span></span>
* <span data-ttu-id="cb151-609">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="cb151-609">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cb151-610">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb151-610">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-611">Az.Resources</span></span>
* <span data-ttu-id="cb151-612">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="cb151-612">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cb151-613">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="cb151-613">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cb151-614">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="cb151-614">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cb151-615">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cb151-615">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cb151-616">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="cb151-616">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cb151-617">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cb151-617">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-618">Az.Sql</span></span>
* <span data-ttu-id="cb151-619">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="cb151-619">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb151-620">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-620">Az.Storage</span></span>
* <span data-ttu-id="cb151-621">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="cb151-621">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cb151-622">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb151-622">New-AzStorageContext</span></span>
* <span data-ttu-id="cb151-623">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="cb151-623">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cb151-624">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb151-624">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb151-625">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cb151-625">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cb151-626">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb151-626">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cb151-627">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb151-627">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cb151-628">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-628">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cb151-629">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb151-629">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb151-630">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cb151-630">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cb151-631">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb151-631">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cb151-632">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cb151-632">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cb151-633">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="cb151-633">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cb151-634">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="cb151-634">Highlights since the last major release</span></span>
* <span data-ttu-id="cb151-635">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="cb151-635">General availability of `Az` module</span></span>
* <span data-ttu-id="cb151-636">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cb151-636">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cb151-637">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cb151-637">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cb151-638">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cb151-638">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cb151-639">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="cb151-639">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb151-640">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-640">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cb151-641">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-641">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb151-642">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb151-642">Az.Automation</span></span>
* <span data-ttu-id="cb151-643">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="cb151-643">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cb151-644">動態分組</span><span class="sxs-lookup"><span data-stu-id="cb151-644">Dynamic grouping</span></span>
    * <span data-ttu-id="cb151-645">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="cb151-645">Pre-Post script</span></span>
    * <span data-ttu-id="cb151-646">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="cb151-646">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-647">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-647">Az.Compute</span></span>
* <span data-ttu-id="cb151-648">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-648">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cb151-649">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="cb151-649">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb151-650">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb151-650">Az.KeyVault</span></span>
* <span data-ttu-id="cb151-651">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cb151-651">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-652">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-652">Az.Network</span></span>
* <span data-ttu-id="cb151-653">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="cb151-653">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cb151-654">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="cb151-654">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-655">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-655">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb151-656">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="cb151-656">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cb151-657">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="cb151-657">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-658">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-658">Az.Resources</span></span>
* <span data-ttu-id="cb151-659">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cb151-659">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cb151-660">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="cb151-660">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-661">Az.Sql</span></span>
* <span data-ttu-id="cb151-662">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="cb151-662">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb151-663">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-663">Az.Storage</span></span>
* <span data-ttu-id="cb151-664">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="cb151-664">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cb151-665">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb151-665">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb151-666">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb151-666">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb151-667">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cb151-667">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cb151-668">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cb151-668">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cb151-669">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cb151-669">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cb151-670">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cb151-670">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-671">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-671">Az.Websites</span></span>
* <span data-ttu-id="cb151-672">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="cb151-672">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="cb151-673">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="cb151-673">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb151-674">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-674">Az.Accounts</span></span>
* <span data-ttu-id="cb151-675">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-675">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cb151-676">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="cb151-676">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb151-677">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb151-677">Az.Automation</span></span>
* <span data-ttu-id="cb151-678">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-678">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb151-679">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="cb151-679">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cb151-680">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="cb151-680">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb151-681">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb151-681">Az.Cdn</span></span>
* <span data-ttu-id="cb151-682">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-682">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-683">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-683">Az.Compute</span></span>
* <span data-ttu-id="cb151-684">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cb151-684">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb151-685">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb151-685">Az.DataFactory</span></span>
* <span data-ttu-id="cb151-686">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="cb151-686">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb151-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb151-687">Az.LogicApp</span></span>
* <span data-ttu-id="cb151-688">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="cb151-688">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-689">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-689">Az.Network</span></span>
* <span data-ttu-id="cb151-690">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="cb151-690">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-691">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-691">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb151-692">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-692">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cb151-693">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="cb151-693">SDK Update</span></span>
* <span data-ttu-id="cb151-694">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="cb151-694">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cb151-695">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="cb151-695">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-696">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-696">Az.Resources</span></span>
* <span data-ttu-id="cb151-697">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-697">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cb151-698">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="cb151-698">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cb151-699">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-699">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cb151-700">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="cb151-700">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cb151-701">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-701">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cb151-702">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="cb151-702">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-703">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-703">Az.Sql</span></span>
* <span data-ttu-id="cb151-704">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="cb151-704">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cb151-705">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="cb151-705">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb151-706">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-706">Az.Storage</span></span>
* <span data-ttu-id="cb151-707">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb151-707">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cb151-708">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="cb151-708">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cb151-709">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb151-709">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb151-710">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-710">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb151-711">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb151-711">Az.Automation</span></span>
* <span data-ttu-id="cb151-712">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="cb151-712">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cb151-713">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-713">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cb151-714">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="cb151-714">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb151-715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb151-715">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb151-716">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="cb151-716">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-717">Az.Compute</span></span>
* <span data-ttu-id="cb151-718">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="cb151-718">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cb151-719">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="cb151-719">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cb151-720">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-720">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cb151-721">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="cb151-721">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb151-722">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-722">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb151-723">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-723">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cb151-724">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cb151-724">Az.EventHub</span></span>
* <span data-ttu-id="cb151-725">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="cb151-725">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="cb151-726">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb151-726">Az.KeyVault</span></span>
* <span data-ttu-id="cb151-727">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="cb151-727">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb151-728">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb151-728">Az.LogicApp</span></span>
* <span data-ttu-id="cb151-729">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="cb151-729">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cb151-730">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="cb151-730">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cb151-731">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-731">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cb151-732">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb151-732">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb151-733">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb151-733">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb151-734">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb151-734">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cb151-735">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cb151-735">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cb151-736">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-736">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cb151-737">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb151-737">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb151-738">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb151-738">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb151-739">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb151-739">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cb151-740">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb151-740">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cb151-741">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="cb151-741">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cb151-742">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb151-742">Az.Monitor</span></span>
* <span data-ttu-id="cb151-743">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="cb151-743">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-744">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-744">Az.Network</span></span>
* <span data-ttu-id="cb151-745">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="cb151-745">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cb151-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="cb151-747">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="cb151-747">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cb151-748">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="cb151-748">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="cb151-749">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="cb151-749">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="cb151-750">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-750">Az.Resources</span></span>
* <span data-ttu-id="cb151-751">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-751">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb151-752">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-752">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cb151-753">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-753">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cb151-754">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="cb151-754">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-755">Az.Sql</span></span>
* <span data-ttu-id="cb151-756">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="cb151-756">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cb151-757">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="cb151-757">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-758">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-758">Az.Websites</span></span>
* <span data-ttu-id="cb151-759">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="cb151-759">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cb151-760">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="cb151-760">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb151-761">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-761">Az.Accounts</span></span>
* <span data-ttu-id="cb151-762">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb151-762">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb151-763">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb151-763">Az.AnalysisServices</span></span>
<span data-ttu-id="cb151-764">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="cb151-764">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-765">Az.Compute</span></span>
* <span data-ttu-id="cb151-766">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-766">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cb151-767">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="cb151-767">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cb151-768">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="cb151-768">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-769">Az.RecoveryServices</span></span>
<span data-ttu-id="cb151-770">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="cb151-770">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-771">Az.Resources</span></span>
* <span data-ttu-id="cb151-772">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="cb151-772">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="cb151-773">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cb151-773">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cb151-774">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-774">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="cb151-775">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cb151-775">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-776">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-776">Az.Sql</span></span>
* <span data-ttu-id="cb151-777">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cb151-777">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cb151-778">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-778">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cb151-779">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="cb151-779">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cb151-780">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="cb151-780">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb151-781">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-781">Az.Accounts</span></span>
* <span data-ttu-id="cb151-782">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="cb151-782">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cb151-783">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cb151-783">Az.AnalysisServices</span></span>
* <span data-ttu-id="cb151-784">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="cb151-784">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-785">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-785">Az.RecoveryServices</span></span>
* <span data-ttu-id="cb151-786">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="cb151-786">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cb151-787">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="cb151-787">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb151-788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-788">Az.Accounts</span></span>
* <span data-ttu-id="cb151-789">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="cb151-789">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cb151-790">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-790">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb151-791">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="cb151-791">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cb151-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cb151-792">Az.Aks</span></span>
* <span data-ttu-id="cb151-793">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-793">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cb151-794">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb151-794">Az.Automation</span></span>
* <span data-ttu-id="cb151-795">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-795">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cb151-796">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-796">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cb151-797">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cb151-797">Az.Cdn</span></span>
* <span data-ttu-id="cb151-798">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-798">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-799">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-799">Az.Compute</span></span>
* <span data-ttu-id="cb151-800">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-800">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cb151-801">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cb151-801">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cb151-802">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="cb151-802">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cb151-803">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cb151-803">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cb151-804">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-804">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cb151-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cb151-805">Az.DataFactory</span></span>
* <span data-ttu-id="cb151-806">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="cb151-806">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb151-807">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-807">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb151-808">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-808">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cb151-809">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="cb151-809">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cb151-810">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-810">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb151-811">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb151-811">Az.IotHub</span></span>
* <span data-ttu-id="cb151-812">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb151-812">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cb151-813">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb151-813">Az.KeyVault</span></span>
* <span data-ttu-id="cb151-814">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-814">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-815">Az.Network</span></span>
* <span data-ttu-id="cb151-816">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-816">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-817">Az.Resources</span></span>
* <span data-ttu-id="cb151-818">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="cb151-818">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cb151-819">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-819">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cb151-820">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="cb151-820">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cb151-821">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-821">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cb151-822">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-822">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cb151-823">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-823">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cb151-824">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="cb151-824">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb151-825">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb151-825">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb151-826">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="cb151-826">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cb151-827">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="cb151-827">Fix some error messages.</span></span>
* <span data-ttu-id="cb151-828">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="cb151-828">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cb151-829">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="cb151-829">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb151-830">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb151-830">Az.SignalR</span></span>
* <span data-ttu-id="cb151-831">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-831">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-832">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-832">Az.Sql</span></span>
* <span data-ttu-id="cb151-833">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-833">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb151-834">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="cb151-834">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cb151-835">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-835">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cb151-836">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="cb151-836">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb151-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-837">Az.Storage</span></span>
* <span data-ttu-id="cb151-838">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-838">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb151-839">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="cb151-839">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cb151-840">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cb151-840">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cb151-841">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cb151-841">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cb151-842">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cb151-842">Az.TrafficManager</span></span>
* <span data-ttu-id="cb151-843">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-843">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-844">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-844">Az.Websites</span></span>
* <span data-ttu-id="cb151-845">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="cb151-845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cb151-846">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="cb151-846">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cb151-847">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="cb151-847">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cb151-848">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="cb151-848">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cb151-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-849">Az.Accounts</span></span>
* <span data-ttu-id="cb151-850">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="cb151-850">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-851">Az.Compute</span></span>
* <span data-ttu-id="cb151-852">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="cb151-852">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cb151-853">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="cb151-853">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cb151-854">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="cb151-854">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb151-855">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-855">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb151-856">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="cb151-856">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cb151-857">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="cb151-857">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cb151-858">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cb151-858">Az.EventGrid</span></span>
* <span data-ttu-id="cb151-859">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="cb151-859">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cb151-860">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="cb151-860">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cb151-861">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="cb151-861">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb151-862">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="cb151-862">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb151-863">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="cb151-863">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb151-864">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="cb151-864">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cb151-865">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="cb151-865">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cb151-866">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="cb151-866">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cb151-867">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="cb151-867">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cb151-868">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="cb151-868">Dead letter endpoint.</span></span>
* <span data-ttu-id="cb151-869">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="cb151-869">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cb151-870">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="cb151-870">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cb151-871">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cb151-871">Az.IotHub</span></span>
* <span data-ttu-id="cb151-872">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="cb151-872">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cb151-873">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cb151-873">Az.LogicApp</span></span>
* <span data-ttu-id="cb151-874">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="cb151-874">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-875">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-875">Az.Resources</span></span>
* <span data-ttu-id="cb151-876">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="cb151-876">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cb151-877">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="cb151-877">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cb151-878">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="cb151-878">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb151-879">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="cb151-879">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cb151-880">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="cb151-880">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cb151-881">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="cb151-881">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cb151-882">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cb151-882">Az.SignalR</span></span>
* <span data-ttu-id="cb151-883">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="cb151-883">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-884">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-884">Az.Sql</span></span>
* <span data-ttu-id="cb151-885">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="cb151-885">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cb151-886">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-886">Az.Storage</span></span>
* <span data-ttu-id="cb151-887">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="cb151-887">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cb151-888">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cb151-888">New-AzStorageContext</span></span>
* <span data-ttu-id="cb151-889">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="cb151-889">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cb151-890">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cb151-890">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-891">Az.Websites</span></span>
* <span data-ttu-id="cb151-892">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="cb151-892">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cb151-893">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="cb151-893">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cb151-894">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="cb151-894">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cb151-895">一般</span><span class="sxs-lookup"><span data-stu-id="cb151-895">General</span></span>

- <span data-ttu-id="cb151-896">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="cb151-896">General Availability of Az Module</span></span>
- <span data-ttu-id="cb151-897">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="cb151-897">Online help for each module</span></span>
- <span data-ttu-id="cb151-898">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="cb151-898">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cb151-899">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-899">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cb151-900">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-900">Az.Accounts</span></span>
- <span data-ttu-id="cb151-901">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="cb151-901">Changed from Az.Profile</span></span>
- <span data-ttu-id="cb151-902">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="cb151-902">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb151-903">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb151-903">Az.ApiManagement</span></span>
- <span data-ttu-id="cb151-904">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="cb151-904">Fixes for #7002</span></span>
- <span data-ttu-id="cb151-905">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-905">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cb151-906">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cb151-906">Az.Batch</span></span>
- <span data-ttu-id="cb151-907">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="cb151-907">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cb151-908">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="cb151-908">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cb151-909">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cb151-910">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cb151-910">Az.Billing</span></span>
- <span data-ttu-id="cb151-911">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-911">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cb151-912">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cb151-912">Az.CognitivServices</span></span>
- <span data-ttu-id="cb151-913">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="cb151-913">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cb151-914">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="cb151-914">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb151-915">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb151-915">Az.ContainerInstance</span></span>
- <span data-ttu-id="cb151-916">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="cb151-916">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cb151-917">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cb151-917">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cb151-918">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-918">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb151-919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-919">Az.DataLakeStore</span></span>
- <span data-ttu-id="cb151-920">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-920">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cb151-921">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cb151-921">Az.Monitor</span></span>
- <span data-ttu-id="cb151-922">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-922">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cb151-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cb151-923">Az.KeyVault</span></span>
- <span data-ttu-id="cb151-924">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="cb151-924">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cb151-925">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cb151-925">Az.MachineLearning</span></span>
- <span data-ttu-id="cb151-926">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-926">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cb151-927">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cb151-927">Az.Media</span></span>
- <span data-ttu-id="cb151-928">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="cb151-928">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb151-929">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-929">Az.Network</span></span>
<span data-ttu-id="cb151-930">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-930">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cb151-931">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="cb151-931">New cmdlets added:</span></span>
        - <span data-ttu-id="cb151-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb151-932">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb151-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb151-933">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb151-934">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb151-934">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb151-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb151-935">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb151-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb151-936">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cb151-937">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cb151-937">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cb151-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cb151-938">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cb151-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb151-939">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cb151-940">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cb151-940">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cb151-941">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb151-941">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cb151-942">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb151-942">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb151-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cb151-943">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cb151-944">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cb151-944">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cb151-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cb151-945">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cb151-946">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="cb151-946">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cb151-947">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-947">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cb151-948">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb151-948">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb151-949">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb151-949">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cb151-950">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cb151-950">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cb151-951">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-951">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cb151-952">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-952">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cb151-953">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-953">Az.OperationalInsights</span></span>
- <span data-ttu-id="cb151-954">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-954">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cb151-955">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb151-955">Az.Profile</span></span>
- <span data-ttu-id="cb151-956">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cb151-956">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-957">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-957">Az.RecoveryServices</span></span>
- <span data-ttu-id="cb151-958">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-958">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cb151-959">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-959">Az.Resources</span></span>
- <span data-ttu-id="cb151-960">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-960">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb151-961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb151-961">Az.ServiceFabric</span></span>
- <span data-ttu-id="cb151-962">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="cb151-962">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cb151-963">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-963">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cb151-964">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cb151-964">Az.SIgnalR</span></span>
- <span data-ttu-id="cb151-965">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="cb151-965">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cb151-966">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-966">Az.Sql</span></span>
- <span data-ttu-id="cb151-967">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="cb151-967">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cb151-968">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="cb151-968">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cb151-969">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-969">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb151-970">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-970">Az.Storage</span></span>
- <span data-ttu-id="cb151-971">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-971">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb151-972">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-972">Az.Websites</span></span>
- <span data-ttu-id="cb151-973">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="cb151-973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cb151-974">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="cb151-974">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cb151-975">一般</span><span class="sxs-lookup"><span data-stu-id="cb151-975">General</span></span>

* <span data-ttu-id="cb151-976">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="cb151-976">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb151-977">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-977">Az.Compute</span></span>

* <span data-ttu-id="cb151-978">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="cb151-978">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cb151-979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-979">Az.DataLakeStore</span></span>

* <span data-ttu-id="cb151-980">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="cb151-980">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cb151-981">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cb151-981">Az.FrontDoor</span></span>

* <span data-ttu-id="cb151-982">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="cb151-982">Fixed some broken links</span></span>
    - <span data-ttu-id="cb151-983">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="cb151-983">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cb151-984">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="cb151-984">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cb151-985">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cb151-985">Az.RecoveryServices</span></span>

* <span data-ttu-id="cb151-986">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="cb151-986">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cb151-987">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="cb151-987">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb151-988">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-988">Az.Resources</span></span>

* <span data-ttu-id="cb151-989">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="cb151-989">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cb151-990">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="cb151-990">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cb151-991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-991">Az.Sql</span></span>

* <span data-ttu-id="cb151-992">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="cb151-992">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cb151-993">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-993">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cb151-994">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="cb151-994">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cb151-995">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-995">Az.Storage</span></span>

* <span data-ttu-id="cb151-996">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="cb151-996">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cb151-997">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="cb151-997">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cb151-998">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb151-998">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb151-999">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="cb151-999">Support Static Website configuration</span></span>
    - <span data-ttu-id="cb151-1000">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb151-1000">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cb151-1001">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cb151-1001">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cb151-1002">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-1002">Az.Websites</span></span>

* <span data-ttu-id="cb151-1003">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cb151-1003">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="cb151-1004">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="cb151-1004">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cb151-1005">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="cb151-1005">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cb151-1006">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="cb151-1006">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cb151-1007">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cb151-1007">Az.ApiManagement</span></span>
* <span data-ttu-id="cb151-1008">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="cb151-1008">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cb151-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cb151-1009">Az.Automation</span></span>
* <span data-ttu-id="cb151-1010">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1010">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cb151-1011">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1011">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cb151-1012">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1012">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cb151-1013">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1013">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cb151-1014">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="cb151-1014">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cb151-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-1015">Az.Compute</span></span>
* <span data-ttu-id="cb151-1016">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1016">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cb151-1017">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="cb151-1017">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cb151-1018">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cb151-1018">Az.ContainerInstance</span></span>
* <span data-ttu-id="cb151-1019">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="cb151-1019">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cb151-1020">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cb151-1020">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cb151-1021">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="cb151-1021">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cb151-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-1022">Az.Network</span></span>
* <span data-ttu-id="cb151-1023">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="cb151-1023">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cb151-1024">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="cb151-1024">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cb151-1025">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="cb151-1025">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="cb151-1026">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1026">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cb151-1027">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cb151-1027">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cb151-1028">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="cb151-1028">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cb151-1029">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="cb151-1029">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cb151-1030">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cb151-1030">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cb151-1031">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="cb151-1031">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cb151-1032">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="cb151-1032">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cb151-1033">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cb151-1033">Az.Relay</span></span>
* <span data-ttu-id="cb151-1034">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="cb151-1034">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cb151-1035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-1035">Az.Resources</span></span>
* <span data-ttu-id="cb151-1036">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="cb151-1036">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cb151-1037">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="cb151-1037">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cb151-1038">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="cb151-1038">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cb151-1039">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb151-1039">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb151-1040">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="cb151-1040">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cb151-1041">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-1041">Az.Sql</span></span>
* <span data-ttu-id="cb151-1042">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1042">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cb151-1043">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb151-1043">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb151-1044">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb151-1044">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb151-1045">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb151-1045">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb151-1046">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cb151-1046">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cb151-1047">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb151-1047">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb151-1048">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb151-1048">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb151-1049">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb151-1049">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cb151-1050">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cb151-1050">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cb151-1051">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="cb151-1051">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cb151-1052">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="cb151-1052">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cb151-1053">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="cb151-1053">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cb151-1054">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="cb151-1054">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb151-1055">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="cb151-1055">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cb151-1056">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="cb151-1056">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cb151-1057">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="cb151-1057">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cb151-1058">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1058">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cb151-1059">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="cb151-1059">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cb151-1060">一般</span><span class="sxs-lookup"><span data-stu-id="cb151-1060">General</span></span>
* <span data-ttu-id="cb151-1061">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="cb151-1061">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cb151-1062">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb151-1062">Az.Profile</span></span>
* <span data-ttu-id="cb151-1063">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb151-1063">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cb151-1064">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="cb151-1064">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cb151-1065">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="cb151-1065">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cb151-1066">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="cb151-1066">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cb151-1067">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1067">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cb151-1068">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1068">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cb151-1069">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1069">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cb151-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb151-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb151-1071">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="cb151-1071">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-1072">Az.Compute</span></span>
* <span data-ttu-id="cb151-1073">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1073">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cb151-1074">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="cb151-1074">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cb151-1075">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="cb151-1075">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb151-1076">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-1076">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb151-1077">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="cb151-1077">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cb151-1078">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="cb151-1078">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cb151-1079">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cb151-1079">Az.Insights</span></span>
* <span data-ttu-id="cb151-1080">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="cb151-1080">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cb151-1081">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="cb151-1081">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cb151-1082">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="cb151-1082">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cb151-1083">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="cb151-1083">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-1084">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-1084">Az.Network</span></span>
* <span data-ttu-id="cb151-1085">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="cb151-1085">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cb151-1086">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb151-1086">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cb151-1087">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cb151-1087">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cb151-1088">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb151-1088">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cb151-1089">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cb151-1089">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cb151-1090">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cb151-1090">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cb151-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cb151-1091">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cb151-1092">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cb151-1092">Az.PolicyInsights</span></span>
* <span data-ttu-id="cb151-1093">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1093">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-1094">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-1094">Az.Resources</span></span>
* <span data-ttu-id="cb151-1095">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="cb151-1095">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cb151-1096">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="cb151-1096">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cb151-1097">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cb151-1097">Az.ServiceBus</span></span>
* <span data-ttu-id="cb151-1098">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="cb151-1098">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cb151-1099">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cb151-1099">Az.ServiceFabric</span></span>
* <span data-ttu-id="cb151-1100">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="cb151-1100">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cb151-1101">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="cb151-1101">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cb151-1102">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="cb151-1102">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cb151-1103">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="cb151-1103">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cb151-1104">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="cb151-1104">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cb151-1105">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="cb151-1105">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cb151-1106">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cb151-1106">Az.Profile</span></span>
* <span data-ttu-id="cb151-1107">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1107">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cb151-1108">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cb151-1108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-1109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-1109">Az.Compute</span></span>
* <span data-ttu-id="cb151-1110">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="cb151-1110">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cb151-1111">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb151-1111">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cb151-1112">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cb151-1112">Az.DataLakeStore</span></span>
* <span data-ttu-id="cb151-1113">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="cb151-1113">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cb151-1114">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="cb151-1114">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cb151-1115">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="cb151-1115">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb151-1116">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="cb151-1116">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cb151-1117">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="cb151-1117">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-1118">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-1118">Az.Network</span></span>
* <span data-ttu-id="cb151-1119">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="cb151-1119">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cb151-1120">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb151-1120">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-1121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-1121">Az.Resources</span></span>
* <span data-ttu-id="cb151-1122">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="cb151-1122">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cb151-1123">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="cb151-1123">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cb151-1124">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="cb151-1124">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cb151-1125">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="cb151-1125">Azure.Storage</span></span>
* <span data-ttu-id="cb151-1126">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1126">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cb151-1127">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cb151-1127">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cb151-1128">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cb151-1128">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cb151-1129">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="cb151-1129">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cb151-1130">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cb151-1130">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="cb151-1131">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cb151-1131">Az.CognitiveServices</span></span>
* <span data-ttu-id="cb151-1132">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="cb151-1132">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cb151-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cb151-1133">Az.Compute</span></span>
* <span data-ttu-id="cb151-1134">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="cb151-1134">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cb151-1135">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="cb151-1135">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cb151-1136">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="cb151-1136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cb151-1137">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cb151-1137">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cb151-1138">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="cb151-1138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cb151-1139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cb151-1139">Az.Network</span></span>
* <span data-ttu-id="cb151-1140">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="cb151-1140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cb151-1141">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1141">new cmdlets added</span></span>
    - <span data-ttu-id="cb151-1142">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb151-1142">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb151-1143">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb151-1143">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb151-1144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb151-1144">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb151-1145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cb151-1145">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cb151-1146">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cb151-1146">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cb151-1147">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb151-1147">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cb151-1148">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="cb151-1148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cb151-1149">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1149">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cb151-1150">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cb151-1150">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cb151-1151">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cb151-1151">Az.RedisCache</span></span>
* <span data-ttu-id="cb151-1152">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="cb151-1152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cb151-1153">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="cb151-1153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cb151-1154">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cb151-1154">Az.Resources</span></span>
* <span data-ttu-id="cb151-1155">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cb151-1155">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cb151-1156">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="cb151-1156">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cb151-1157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cb151-1157">Az.Sql</span></span>
* <span data-ttu-id="cb151-1158">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="cb151-1158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cb151-1159">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cb151-1159">Az.Websites</span></span>
* <span data-ttu-id="cb151-1160">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="cb151-1160">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cb151-1161">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="cb151-1161">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cb151-1162">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="cb151-1162">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cb151-1163">初始版本</span><span class="sxs-lookup"><span data-stu-id="cb151-1163">Initial Release</span></span>