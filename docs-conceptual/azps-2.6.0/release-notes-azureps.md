---
ms.openlocfilehash: f89d13d6bbedaea29b62287942d8c7a509abe32b
ms.sourcegitcommit: abca342d8687ca638679c049792d0cef6045837d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/27/2019
ms.locfileid: "70052629"
---
## <a name="260---august-2019"></a><span data-ttu-id="f36fd-101">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-101">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f36fd-102">一般</span><span class="sxs-lookup"><span data-stu-id="f36fd-102">General</span></span>
* <span data-ttu-id="f36fd-103">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-103">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f36fd-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-104">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-105">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="f36fd-105">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f36fd-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f36fd-106">Az.Aks</span></span>
* <span data-ttu-id="f36fd-107">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-107">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f36fd-108">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f36fd-108">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f36fd-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f36fd-109">Az.ApiManagement</span></span>
* <span data-ttu-id="f36fd-110">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-110">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f36fd-111">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="f36fd-111">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f36fd-112">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-112">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f36fd-113">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f36fd-113">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f36fd-114">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="f36fd-114">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f36fd-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f36fd-115">Az.Batch</span></span>
* <span data-ttu-id="f36fd-116">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="f36fd-116">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f36fd-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f36fd-117">Az.Cdn</span></span>
* <span data-ttu-id="f36fd-118">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-118">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-119">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-119">Az.Compute</span></span>
* <span data-ttu-id="f36fd-120">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-120">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f36fd-121">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="f36fd-121">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f36fd-122">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="f36fd-122">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f36fd-123">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="f36fd-123">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f36fd-124">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f36fd-124">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f36fd-125">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="f36fd-125">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f36fd-126">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f36fd-126">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f36fd-127">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-127">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36fd-128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36fd-128">Az.DataFactory</span></span>
* <span data-ttu-id="f36fd-129">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="f36fd-129">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f36fd-130">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="f36fd-130">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f36fd-131">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="f36fd-131">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f36fd-132">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="f36fd-132">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-133">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-133">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36fd-134">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f36fd-134">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f36fd-135">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-135">Az.EventHub</span></span>
* <span data-ttu-id="f36fd-136">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-136">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f36fd-137">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="f36fd-137">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f36fd-138">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-138">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f36fd-139">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="f36fd-139">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f36fd-140">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f36fd-140">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f36fd-141">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-141">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f36fd-142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36fd-142">Az.Monitor</span></span>
* <span data-ttu-id="f36fd-143">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f36fd-143">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-144">Az.Network</span></span>
* <span data-ttu-id="f36fd-145">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-145">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f36fd-146">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="f36fd-146">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f36fd-147">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="f36fd-147">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f36fd-148">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-148">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f36fd-149">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="f36fd-149">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="f36fd-150">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="f36fd-150">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f36fd-151">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-151">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f36fd-152">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-152">Az.OperationalInsights</span></span>
* <span data-ttu-id="f36fd-153">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="f36fd-153">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f36fd-154">新增了範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-154">Added example</span></span>
    - <span data-ttu-id="f36fd-155">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="f36fd-155">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f36fd-156">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-156">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f36fd-157">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-157">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-159">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-159">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-160">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-160">Az.Resources</span></span>
* <span data-ttu-id="f36fd-161">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-161">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f36fd-162">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-162">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f36fd-163">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="f36fd-163">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f36fd-164">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-164">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f36fd-165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f36fd-165">Az.ServiceBus</span></span>
* <span data-ttu-id="f36fd-166">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-166">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f36fd-167">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="f36fd-167">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f36fd-168">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="f36fd-168">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="f36fd-169">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36fd-169">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36fd-170">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="f36fd-170">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f36fd-171">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-171">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f36fd-172">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f36fd-172">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f36fd-173">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-173">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f36fd-174">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f36fd-174">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f36fd-175">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-175">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-176">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-176">Az.Sql</span></span>
* <span data-ttu-id="f36fd-177">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="f36fd-177">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-178">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-178">Az.Storage</span></span>
* <span data-ttu-id="f36fd-179">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-179">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f36fd-180">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="f36fd-180">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f36fd-181">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f36fd-181">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f36fd-182">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f36fd-182">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f36fd-183">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="f36fd-183">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f36fd-184">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f36fd-184">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-185">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-185">Az.Websites</span></span>
* <span data-ttu-id="f36fd-186">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="f36fd-186">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f36fd-187">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-187">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-188">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-189">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f36fd-189">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f36fd-190">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-190">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f36fd-191">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-191">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="f36fd-192">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-192">Az.Automation</span></span>
* <span data-ttu-id="f36fd-193">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-193">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36fd-194">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-194">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36fd-195">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-195">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-196">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-196">Az.Compute</span></span>
* <span data-ttu-id="f36fd-197">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-197">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f36fd-198">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f36fd-198">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f36fd-199">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-199">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f36fd-200">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f36fd-200">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36fd-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36fd-201">Az.DataFactory</span></span>
* <span data-ttu-id="f36fd-202">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f36fd-202">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f36fd-203">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-203">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f36fd-204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-204">Az.EventHub</span></span>
* <span data-ttu-id="f36fd-205">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f36fd-205">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f36fd-206">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f36fd-206">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f36fd-207">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36fd-207">Az.KeyVault</span></span>
* <span data-ttu-id="f36fd-208">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-208">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f36fd-209">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f36fd-209">Az.LogicApp</span></span>
* <span data-ttu-id="f36fd-210">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="f36fd-210">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f36fd-211">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="f36fd-211">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f36fd-212">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-212">Az.ManagedServices</span></span>
* <span data-ttu-id="f36fd-213">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-213">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-214">Az.Network</span></span>
* <span data-ttu-id="f36fd-215">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-215">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f36fd-216">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-216">New cmdlets</span></span>
        - <span data-ttu-id="f36fd-217">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f36fd-217">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f36fd-218">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f36fd-218">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f36fd-219">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f36fd-219">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f36fd-220">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f36fd-220">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f36fd-221">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f36fd-221">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f36fd-222">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f36fd-222">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f36fd-223">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f36fd-223">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f36fd-224">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f36fd-224">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f36fd-225">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="f36fd-225">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f36fd-226">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-226">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f36fd-227">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，指出此子網路中的私人端點是啟用或停用套用網路原則。</span><span class="sxs-lookup"><span data-stu-id="f36fd-227">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="f36fd-228">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，指出此子網路中的私人連結服務是啟用或停用套用網路原則。</span><span class="sxs-lookup"><span data-stu-id="f36fd-228">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f36fd-229">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="f36fd-229">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f36fd-230">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="f36fd-230">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f36fd-231">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-231">Updated cmdlets</span></span>
        - <span data-ttu-id="f36fd-232">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-232">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f36fd-233">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-233">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f36fd-234">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-234">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f36fd-235">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="f36fd-235">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f36fd-236">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f36fd-236">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f36fd-237">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f36fd-237">Updated cmdlet:</span></span>
        - <span data-ttu-id="f36fd-238">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-238">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f36fd-239">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-239">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f36fd-240">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-240">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f36fd-241">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="f36fd-241">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f36fd-242">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="f36fd-242">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f36fd-243">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="f36fd-243">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f36fd-244">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-244">Az.OperationalInsights</span></span>
* <span data-ttu-id="f36fd-245">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="f36fd-245">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="f36fd-246">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="f36fd-246">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-248">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-248">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f36fd-249">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-249">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f36fd-250">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-250">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f36fd-251">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-251">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f36fd-252">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-252">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f36fd-253">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-253">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f36fd-254">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-254">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f36fd-255">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-255">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f36fd-256">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="f36fd-256">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f36fd-257">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="f36fd-257">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-258">Az.Resources</span></span>
- <span data-ttu-id="f36fd-259">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-259">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f36fd-260">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f36fd-260">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f36fd-261">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f36fd-261">Az.ServiceBus</span></span>
* <span data-ttu-id="f36fd-262">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f36fd-262">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f36fd-263">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f36fd-263">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-264">Az.Sql</span></span>
* <span data-ttu-id="f36fd-265">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-265">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f36fd-266">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-266">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f36fd-267">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="f36fd-267">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-268">Az.Storage</span></span>
* <span data-ttu-id="f36fd-269">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f36fd-269">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f36fd-270">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f36fd-270">Az.StorageSync</span></span>
* <span data-ttu-id="f36fd-271">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f36fd-271">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f36fd-272">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="f36fd-272">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-273">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-273">Az.Websites</span></span>
* <span data-ttu-id="f36fd-274">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f36fd-274">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f36fd-275">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="f36fd-275">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f36fd-276">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f36fd-276">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f36fd-277">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-277">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-278">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-278">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-279">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-279">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f36fd-280">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-280">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f36fd-281">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-281">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f36fd-282">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f36fd-282">Az.Advisor</span></span>
* <span data-ttu-id="f36fd-283">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="f36fd-283">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f36fd-284">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="f36fd-284">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f36fd-285">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f36fd-285">Az.ApiManagement</span></span>
* <span data-ttu-id="f36fd-286">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-286">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f36fd-287">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f36fd-287">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f36fd-288">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-288">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f36fd-289">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-289">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f36fd-290">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-290">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f36fd-291">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f36fd-291">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f36fd-292">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-292">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36fd-293">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-293">Az.Automation</span></span>
* <span data-ttu-id="f36fd-294">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="f36fd-294">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-295">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-295">Az.Compute</span></span>
* <span data-ttu-id="f36fd-296">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-296">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36fd-297">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36fd-297">Az.DataFactory</span></span>
* <span data-ttu-id="f36fd-298">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="f36fd-298">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f36fd-299">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f36fd-299">Az.EventGrid</span></span>
* <span data-ttu-id="f36fd-300">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-300">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f36fd-301">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-301">Az.IotHub</span></span>
* <span data-ttu-id="f36fd-302">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-302">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-303">Az.Network</span></span>
* <span data-ttu-id="f36fd-304">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="f36fd-304">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f36fd-305">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-305">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f36fd-306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-306">Az.PolicyInsights</span></span>
* <span data-ttu-id="f36fd-307">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-307">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f36fd-308">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f36fd-308">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f36fd-309">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-309">Az.OperationalInsights</span></span>
* <span data-ttu-id="f36fd-310">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="f36fd-310">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-311">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-311">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-312">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="f36fd-312">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-313">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-313">Az.Resources</span></span>
    - <span data-ttu-id="f36fd-314">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="f36fd-314">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f36fd-315">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-315">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f36fd-316">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="f36fd-316">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f36fd-317">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="f36fd-317">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f36fd-318">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f36fd-318">Az.ServiceBus</span></span>
* <span data-ttu-id="f36fd-319">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="f36fd-319">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-320">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-320">Az.Sql</span></span>
* <span data-ttu-id="f36fd-321">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="f36fd-321">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f36fd-322">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="f36fd-322">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f36fd-323">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f36fd-323">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f36fd-324">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f36fd-324">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f36fd-325">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f36fd-325">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f36fd-326">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f36fd-326">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f36fd-327">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f36fd-327">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f36fd-328">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f36fd-328">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f36fd-329">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="f36fd-329">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-330">Az.Storage</span></span>
* <span data-ttu-id="f36fd-331">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="f36fd-331">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f36fd-332">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f36fd-332">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f36fd-333">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="f36fd-333">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f36fd-334">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="f36fd-334">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f36fd-335">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="f36fd-335">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f36fd-336">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36fd-336">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f36fd-337">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36fd-337">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f36fd-338">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="f36fd-338">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f36fd-339">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f36fd-339">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f36fd-340">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f36fd-340">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f36fd-341">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f36fd-341">Az.StorageSync</span></span>
* <span data-ttu-id="f36fd-342">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="f36fd-342">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f36fd-343">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-343">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-344">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-344">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-345">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f36fd-345">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f36fd-346">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f36fd-346">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f36fd-347">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-347">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f36fd-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f36fd-348">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f36fd-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f36fd-349">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-350">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-350">Az.Compute</span></span>
* <span data-ttu-id="f36fd-351">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="f36fd-351">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f36fd-352">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-352">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f36fd-353">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f36fd-353">Az.Dns</span></span>
* <span data-ttu-id="f36fd-354">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="f36fd-354">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f36fd-355">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f36fd-355">Az.EventGrid</span></span>
* <span data-ttu-id="f36fd-356">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f36fd-356">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f36fd-357">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f36fd-357">New cmdlets:</span></span>
    - <span data-ttu-id="f36fd-358">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f36fd-358">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f36fd-359">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="f36fd-359">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f36fd-360">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f36fd-360">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f36fd-361">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="f36fd-361">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f36fd-362">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f36fd-362">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f36fd-363">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="f36fd-363">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f36fd-364">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f36fd-364">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f36fd-365">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="f36fd-365">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f36fd-366">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f36fd-366">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f36fd-367">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="f36fd-367">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f36fd-368">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="f36fd-368">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f36fd-369">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-369">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f36fd-370">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f36fd-370">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f36fd-371">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="f36fd-371">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="f36fd-372">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="f36fd-372">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f36fd-373">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-373">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f36fd-374">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f36fd-374">Updated cmdlets:</span></span>
    - <span data-ttu-id="f36fd-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="f36fd-375">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f36fd-376">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f36fd-376">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f36fd-377">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f36fd-377">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f36fd-378">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-378">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f36fd-379">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="f36fd-379">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f36fd-380">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="f36fd-380">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f36fd-381">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="f36fd-381">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f36fd-382">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="f36fd-382">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f36fd-383">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="f36fd-383">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="f36fd-384">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="f36fd-384">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f36fd-385">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="f36fd-385">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f36fd-386">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f36fd-386">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f36fd-387">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f36fd-387">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f36fd-388">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="f36fd-388">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f36fd-389">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f36fd-389">Az.FrontDoor</span></span>
* <span data-ttu-id="f36fd-390">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f36fd-390">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f36fd-391">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f36fd-391">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f36fd-392">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f36fd-392">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f36fd-393">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="f36fd-393">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-394">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-394">Az.Network</span></span>
* <span data-ttu-id="f36fd-395">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-395">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f36fd-396">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-396">New cmdlets</span></span>
        - <span data-ttu-id="f36fd-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f36fd-397">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f36fd-398">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f36fd-398">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f36fd-399">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-399">New cmdlets</span></span> 
        - <span data-ttu-id="f36fd-400">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f36fd-400">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f36fd-401">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f36fd-401">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f36fd-402">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-402">New cmdlets</span></span> 
        - <span data-ttu-id="f36fd-403">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f36fd-403">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="f36fd-404">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f36fd-404">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f36fd-405">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f36fd-405">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f36fd-406">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-406">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f36fd-407">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f36fd-407">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f36fd-408">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f36fd-408">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f36fd-409">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-409">New cmdlets</span></span>
        - <span data-ttu-id="f36fd-410">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f36fd-410">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f36fd-411">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f36fd-411">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f36fd-412">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f36fd-412">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f36fd-413">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f36fd-413">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f36fd-414">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="f36fd-414">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f36fd-415">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="f36fd-415">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f36fd-416">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="f36fd-416">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f36fd-417">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="f36fd-417">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f36fd-418">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="f36fd-418">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f36fd-419">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="f36fd-419">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f36fd-420">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="f36fd-420">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f36fd-421">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="f36fd-421">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f36fd-422">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-422">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f36fd-423">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="f36fd-423">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f36fd-424">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="f36fd-424">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f36fd-425">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-425">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f36fd-426">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="f36fd-426">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f36fd-427">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-427">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f36fd-428">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f36fd-428">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f36fd-429">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="f36fd-429">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f36fd-430">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="f36fd-430">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f36fd-431">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="f36fd-431">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f36fd-432">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="f36fd-432">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="f36fd-433">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="f36fd-433">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="f36fd-434">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="f36fd-434">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f36fd-435">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="f36fd-435">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f36fd-436">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="f36fd-436">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f36fd-437">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-437">Az.OperationalInsights</span></span>
* <span data-ttu-id="f36fd-438">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="f36fd-438">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-439">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-439">Az.Resources</span></span>
* <span data-ttu-id="f36fd-440">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="f36fd-440">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f36fd-441">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f36fd-441">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f36fd-442">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f36fd-442">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f36fd-443">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="f36fd-443">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f36fd-444">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36fd-444">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36fd-445">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-445">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-446">Az.Sql</span></span>
* <span data-ttu-id="f36fd-447">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="f36fd-447">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f36fd-448">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="f36fd-448">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f36fd-449">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="f36fd-449">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f36fd-450">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f36fd-450">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f36fd-451">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f36fd-451">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f36fd-452">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f36fd-452">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f36fd-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f36fd-453">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f36fd-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f36fd-454">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-455">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-455">Az.Storage</span></span>
* <span data-ttu-id="f36fd-456">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="f36fd-456">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f36fd-457">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36fd-457">New-AzStorageAccount</span></span>
* <span data-ttu-id="f36fd-458">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="f36fd-458">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f36fd-459">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f36fd-459">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-460">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-460">Az.Websites</span></span>
* <span data-ttu-id="f36fd-461">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="f36fd-461">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f36fd-462">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f36fd-462">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f36fd-463">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-463">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f36fd-464">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f36fd-464">Az.Cdn</span></span>
* <span data-ttu-id="f36fd-465">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="f36fd-465">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-466">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-466">Az.Compute</span></span>
* <span data-ttu-id="f36fd-467">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="f36fd-467">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f36fd-468">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f36fd-468">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f36fd-469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-469">Az.EventHub</span></span>
* <span data-ttu-id="f36fd-470">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="f36fd-470">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f36fd-471">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36fd-471">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-472">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-472">Az.Network</span></span>
* <span data-ttu-id="f36fd-473">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="f36fd-473">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f36fd-474">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="f36fd-474">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f36fd-475">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-475">Az.PolicyInsights</span></span>
* <span data-ttu-id="f36fd-476">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-476">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-477">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-478">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="f36fd-478">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f36fd-479">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f36fd-479">Az.ServiceBus</span></span>
* <span data-ttu-id="f36fd-480">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36fd-480">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f36fd-481">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36fd-481">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36fd-482">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-482">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f36fd-483">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="f36fd-483">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-484">Az.Sql</span></span>
* <span data-ttu-id="f36fd-485">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="f36fd-485">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f36fd-486">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-486">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f36fd-487">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="f36fd-487">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f36fd-488">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="f36fd-488">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-489">Az.Websites</span></span>
* <span data-ttu-id="f36fd-490">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-490">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f36fd-491">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-491">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f36fd-492">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f36fd-492">Az.ApiManagement</span></span>
* <span data-ttu-id="f36fd-493">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="f36fd-493">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f36fd-494">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="f36fd-494">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f36fd-495">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="f36fd-495">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f36fd-496">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="f36fd-496">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f36fd-497">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="f36fd-497">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f36fd-498">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="f36fd-498">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f36fd-499">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="f36fd-499">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f36fd-500">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="f36fd-500">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f36fd-501">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="f36fd-501">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f36fd-502">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="f36fd-502">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f36fd-503">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="f36fd-503">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f36fd-504">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="f36fd-504">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f36fd-505">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="f36fd-505">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f36fd-506">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-506">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f36fd-507">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-507">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f36fd-508">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-508">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f36fd-509">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-509">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f36fd-510">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-510">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f36fd-511">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="f36fd-511">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="f36fd-512">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="f36fd-512">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f36fd-513">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="f36fd-513">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f36fd-514">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="f36fd-514">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f36fd-515">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="f36fd-515">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f36fd-516">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="f36fd-516">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="f36fd-517">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-517">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f36fd-518">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-518">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f36fd-519">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="f36fd-519">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f36fd-520">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="f36fd-520">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f36fd-521">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-521">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f36fd-522">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="f36fd-522">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f36fd-523">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f36fd-523">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="f36fd-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f36fd-524">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f36fd-525">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="f36fd-525">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f36fd-526">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f36fd-526">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f36fd-527">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="f36fd-527">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f36fd-528">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="f36fd-528">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f36fd-529">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="f36fd-529">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f36fd-530">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="f36fd-530">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f36fd-531">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="f36fd-531">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f36fd-532">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f36fd-532">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="f36fd-533">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="f36fd-533">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f36fd-534">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="f36fd-534">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f36fd-535">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="f36fd-535">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f36fd-536">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="f36fd-536">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f36fd-537">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f36fd-537">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f36fd-538">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="f36fd-538">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f36fd-539">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="f36fd-539">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="f36fd-540">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="f36fd-540">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="f36fd-541">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="f36fd-541">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f36fd-542">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="f36fd-542">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f36fd-543">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="f36fd-543">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f36fd-544">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="f36fd-544">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f36fd-545">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="f36fd-545">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f36fd-546">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="f36fd-546">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f36fd-547">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="f36fd-547">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f36fd-548">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="f36fd-548">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f36fd-549">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f36fd-549">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f36fd-550">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="f36fd-550">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f36fd-551">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="f36fd-551">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f36fd-552">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-552">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f36fd-553">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f36fd-553">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f36fd-554">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="f36fd-554">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f36fd-555">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="f36fd-555">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f36fd-556">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-556">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f36fd-557">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="f36fd-557">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f36fd-558">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="f36fd-558">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f36fd-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f36fd-559">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f36fd-560">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="f36fd-560">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f36fd-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f36fd-561">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f36fd-562">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f36fd-562">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f36fd-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f36fd-563">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f36fd-564">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="f36fd-564">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f36fd-565">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="f36fd-565">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f36fd-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f36fd-566">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f36fd-567">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="f36fd-567">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="f36fd-568">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f36fd-568">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f36fd-569">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="f36fd-569">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36fd-570">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-570">Az.Automation</span></span>
* <span data-ttu-id="f36fd-571">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="f36fd-571">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f36fd-572">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-572">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f36fd-573">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-573">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f36fd-574">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="f36fd-574">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f36fd-575">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-575">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f36fd-576">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-576">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f36fd-577">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="f36fd-577">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-578">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-578">Az.Compute</span></span>
* <span data-ttu-id="f36fd-579">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f36fd-579">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f36fd-580">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="f36fd-580">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-581">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-581">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36fd-582">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="f36fd-582">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f36fd-583">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36fd-583">Az.Monitor</span></span>
* <span data-ttu-id="f36fd-584">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="f36fd-584">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-585">Az.Network</span></span>
* <span data-ttu-id="f36fd-586">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="f36fd-586">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f36fd-587">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f36fd-587">Updated cmdlet:</span></span>
        - <span data-ttu-id="f36fd-588">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f36fd-588">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f36fd-589">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="f36fd-589">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-590">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-590">Az.Resources</span></span>
* <span data-ttu-id="f36fd-591">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="f36fd-591">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-592">Az.Sql</span></span>
* <span data-ttu-id="f36fd-593">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="f36fd-593">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f36fd-594">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-594">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-595">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-596">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-596">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36fd-597">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-597">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36fd-598">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="f36fd-598">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f36fd-599">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f36fd-599">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-600">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-600">Az.Compute</span></span>
* <span data-ttu-id="f36fd-601">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="f36fd-601">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f36fd-602">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f36fd-602">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f36fd-603">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-603">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f36fd-604">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="f36fd-604">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f36fd-605">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="f36fd-605">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f36fd-606">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f36fd-606">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="f36fd-607">重大變更</span><span class="sxs-lookup"><span data-stu-id="f36fd-607">Breaking changes</span></span>
    - <span data-ttu-id="f36fd-608">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="f36fd-608">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f36fd-609">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="f36fd-609">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f36fd-610">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f36fd-610">Az.DeploymentManager</span></span>
* <span data-ttu-id="f36fd-611">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-611">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f36fd-612">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f36fd-612">Az.Dns</span></span>
* <span data-ttu-id="f36fd-613">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="f36fd-613">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f36fd-614">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="f36fd-614">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f36fd-615">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="f36fd-615">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f36fd-616">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f36fd-616">Az.FrontDoor</span></span>
* <span data-ttu-id="f36fd-617">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-617">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f36fd-618">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="f36fd-618">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f36fd-619">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f36fd-619">Az.HDInsight</span></span>
* <span data-ttu-id="f36fd-620">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f36fd-620">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f36fd-621">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f36fd-621">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f36fd-622">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f36fd-622">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f36fd-623">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f36fd-623">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f36fd-624">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="f36fd-624">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f36fd-625">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f36fd-625">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f36fd-626">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="f36fd-626">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f36fd-627">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36fd-627">Az.Monitor</span></span>
* <span data-ttu-id="f36fd-628">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="f36fd-628">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="f36fd-629">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f36fd-629">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f36fd-630">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f36fd-630">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f36fd-631">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f36fd-631">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f36fd-632">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f36fd-632">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f36fd-633">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f36fd-633">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f36fd-634">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f36fd-634">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f36fd-635">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-635">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36fd-636">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-636">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36fd-637">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-637">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36fd-638">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-638">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36fd-639">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-639">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f36fd-640">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f36fd-640">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f36fd-641">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-641">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-642">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-642">Az.Network</span></span>
* <span data-ttu-id="f36fd-643">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-643">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f36fd-644">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-644">New cmdlets</span></span>
        - <span data-ttu-id="f36fd-645">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f36fd-645">New-AzNatGateway</span></span>
        - <span data-ttu-id="f36fd-646">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f36fd-646">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f36fd-647">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f36fd-647">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f36fd-648">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f36fd-648">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f36fd-649">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-649">Updated cmdlets</span></span>
        - <span data-ttu-id="f36fd-650">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f36fd-650">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f36fd-651">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f36fd-651">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f36fd-652">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f36fd-652">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f36fd-653">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f36fd-653">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f36fd-654">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="f36fd-654">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f36fd-655">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-655">Az.PolicyInsights</span></span>
* <span data-ttu-id="f36fd-656">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f36fd-656">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f36fd-657">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="f36fd-657">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f36fd-658">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="f36fd-658">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-659">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-659">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-660">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="f36fd-660">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f36fd-661">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="f36fd-661">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f36fd-662">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="f36fd-662">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f36fd-663">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="f36fd-663">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f36fd-664">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="f36fd-664">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f36fd-665">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="f36fd-665">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f36fd-666">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f36fd-666">Az.Relay</span></span>
* <span data-ttu-id="f36fd-667">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-667">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f36fd-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f36fd-668">Az.ServiceBus</span></span>
* <span data-ttu-id="f36fd-669">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-669">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-670">Az.Storage</span></span>
* <span data-ttu-id="f36fd-671">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="f36fd-671">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f36fd-672">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="f36fd-672">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f36fd-673">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="f36fd-673">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f36fd-674">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36fd-674">New-AzStorageAccount</span></span>
* <span data-ttu-id="f36fd-675">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="f36fd-675">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f36fd-676">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36fd-676">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f36fd-677">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36fd-677">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f36fd-678">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36fd-678">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-679">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-679">Az.Websites</span></span>
* <span data-ttu-id="f36fd-680">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="f36fd-680">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f36fd-681">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="f36fd-681">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f36fd-682">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-682">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f36fd-683">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f36fd-683">Highlights since the last major release</span></span>
* <span data-ttu-id="f36fd-684">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="f36fd-684">General availability of `Az` module</span></span>
* <span data-ttu-id="f36fd-685">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f36fd-685">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f36fd-686">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f36fd-686">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f36fd-687">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-687">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f36fd-688">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="f36fd-688">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f36fd-689">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-689">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f36fd-690">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-690">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f36fd-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-691">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-692">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="f36fd-692">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f36fd-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f36fd-693">Az.Batch</span></span>
* <span data-ttu-id="f36fd-694">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-694">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f36fd-695">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f36fd-695">Az.Cdn</span></span>
* <span data-ttu-id="f36fd-696">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-696">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36fd-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36fd-698">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-698">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-699">Az.Compute</span></span>
* <span data-ttu-id="f36fd-700">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-700">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f36fd-701">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-701">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36fd-702">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f36fd-702">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36fd-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36fd-703">Az.DataFactory</span></span>
* <span data-ttu-id="f36fd-704">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="f36fd-704">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-705">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-705">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36fd-706">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-706">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f36fd-707">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f36fd-707">Az.EventGrid</span></span>
* <span data-ttu-id="f36fd-708">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f36fd-708">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f36fd-709">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-709">Az.EventHub</span></span>
* <span data-ttu-id="f36fd-710">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-710">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="f36fd-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f36fd-711">Az.HDInsight</span></span>
* <span data-ttu-id="f36fd-712">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-712">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f36fd-713">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-713">Az.IotHub</span></span>
* <span data-ttu-id="f36fd-714">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-714">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f36fd-715">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36fd-715">Az.KeyVault</span></span>
* <span data-ttu-id="f36fd-716">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-716">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36fd-717">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f36fd-717">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f36fd-718">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f36fd-718">Az.MachineLearning</span></span>
* <span data-ttu-id="f36fd-719">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-719">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f36fd-720">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f36fd-720">Az.Media</span></span>
* <span data-ttu-id="f36fd-721">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-721">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f36fd-722">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36fd-722">Az.Monitor</span></span>
  * <span data-ttu-id="f36fd-723">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-723">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f36fd-724">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f36fd-724">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f36fd-725">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f36fd-725">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f36fd-726">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f36fd-726">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f36fd-727">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f36fd-727">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f36fd-728">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f36fd-728">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f36fd-729">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="f36fd-729">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-730">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-730">Az.Network</span></span>
* <span data-ttu-id="f36fd-731">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-731">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36fd-732">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f36fd-732">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f36fd-733">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f36fd-733">Az.NotificationHubs</span></span>
* <span data-ttu-id="f36fd-734">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-734">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f36fd-735">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-735">Az.OperationalInsights</span></span>
* <span data-ttu-id="f36fd-736">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-736">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f36fd-737">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f36fd-737">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f36fd-738">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-738">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-739">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-739">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-740">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-740">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36fd-741">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="f36fd-741">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f36fd-742">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="f36fd-742">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f36fd-743">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="f36fd-743">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f36fd-744">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f36fd-744">Az.RedisCache</span></span>
* <span data-ttu-id="f36fd-745">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-745">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-746">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-746">Az.Resources</span></span>
* <span data-ttu-id="f36fd-747">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f36fd-747">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-748">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-748">Az.Sql</span></span>
* <span data-ttu-id="f36fd-749">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="f36fd-749">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f36fd-750">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-750">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36fd-751">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="f36fd-751">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f36fd-752">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="f36fd-752">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f36fd-753">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f36fd-753">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f36fd-754">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="f36fd-754">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f36fd-755">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="f36fd-755">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-756">Az.Websites</span></span>
* <span data-ttu-id="f36fd-757">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="f36fd-757">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f36fd-758">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-758">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f36fd-759">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="f36fd-759">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f36fd-760">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="f36fd-760">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f36fd-761">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-761">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f36fd-762">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f36fd-762">Highlights since the last major release</span></span>
* <span data-ttu-id="f36fd-763">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="f36fd-763">General availability of `Az` module</span></span>
* <span data-ttu-id="f36fd-764">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f36fd-764">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f36fd-765">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f36fd-765">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f36fd-766">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-766">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f36fd-767">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="f36fd-767">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f36fd-768">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-768">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f36fd-769">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-769">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f36fd-770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-770">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-771">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="f36fd-771">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f36fd-772">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-772">Az.AnalysisServices</span></span>
* <span data-ttu-id="f36fd-773">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="f36fd-773">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f36fd-774">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="f36fd-774">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36fd-775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-775">Az.Automation</span></span>
* <span data-ttu-id="f36fd-776">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-776">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f36fd-777">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="f36fd-777">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f36fd-778">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="f36fd-778">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-779">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-779">Az.Compute</span></span>
* <span data-ttu-id="f36fd-780">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-780">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f36fd-781">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="f36fd-781">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="f36fd-782">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f36fd-782">Az.ContainerInstance</span></span>
* <span data-ttu-id="f36fd-783">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="f36fd-783">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36fd-784">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36fd-784">Az.DataFactory</span></span>
* <span data-ttu-id="f36fd-785">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="f36fd-785">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f36fd-786">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f36fd-786">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-787">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-787">Az.Resources</span></span>
* <span data-ttu-id="f36fd-788">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="f36fd-788">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f36fd-789">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="f36fd-789">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f36fd-790">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="f36fd-790">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f36fd-791">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f36fd-791">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f36fd-792">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="f36fd-792">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f36fd-793">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f36fd-793">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-794">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-794">Az.Sql</span></span>
* <span data-ttu-id="f36fd-795">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="f36fd-795">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-796">Az.Storage</span></span>
* <span data-ttu-id="f36fd-797">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="f36fd-797">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f36fd-798">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f36fd-798">New-AzStorageContext</span></span>
* <span data-ttu-id="f36fd-799">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="f36fd-799">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f36fd-800">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f36fd-800">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f36fd-801">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f36fd-801">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f36fd-802">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f36fd-802">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f36fd-803">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f36fd-803">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f36fd-804">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-804">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f36fd-805">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f36fd-805">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f36fd-806">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f36fd-806">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f36fd-807">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f36fd-807">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f36fd-808">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f36fd-808">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f36fd-809">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-809">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f36fd-810">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="f36fd-810">Highlights since the last major release</span></span>
* <span data-ttu-id="f36fd-811">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="f36fd-811">General availability of `Az` module</span></span>
* <span data-ttu-id="f36fd-812">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f36fd-812">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f36fd-813">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f36fd-813">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f36fd-814">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-814">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f36fd-815">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="f36fd-815">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f36fd-816">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-816">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f36fd-817">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-817">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36fd-818">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-818">Az.Automation</span></span>
* <span data-ttu-id="f36fd-819">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="f36fd-819">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f36fd-820">動態分組</span><span class="sxs-lookup"><span data-stu-id="f36fd-820">Dynamic grouping</span></span>
    * <span data-ttu-id="f36fd-821">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="f36fd-821">Pre-Post script</span></span>
    * <span data-ttu-id="f36fd-822">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="f36fd-822">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-823">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-823">Az.Compute</span></span>
* <span data-ttu-id="f36fd-824">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-824">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f36fd-825">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="f36fd-825">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f36fd-826">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36fd-826">Az.KeyVault</span></span>
* <span data-ttu-id="f36fd-827">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-827">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-828">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-828">Az.Network</span></span>
* <span data-ttu-id="f36fd-829">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-829">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f36fd-830">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="f36fd-830">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-831">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-831">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-832">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="f36fd-832">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f36fd-833">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-833">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-834">Az.Resources</span></span>
* <span data-ttu-id="f36fd-835">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-835">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f36fd-836">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="f36fd-836">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-837">Az.Sql</span></span>
* <span data-ttu-id="f36fd-838">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="f36fd-838">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-839">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-839">Az.Storage</span></span>
* <span data-ttu-id="f36fd-840">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="f36fd-840">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f36fd-841">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f36fd-841">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f36fd-842">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f36fd-842">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f36fd-843">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f36fd-843">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f36fd-844">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f36fd-844">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f36fd-845">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f36fd-845">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f36fd-846">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-846">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-847">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-847">Az.Websites</span></span>
* <span data-ttu-id="f36fd-848">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="f36fd-848">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="f36fd-849">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-849">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-850">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-850">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-851">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-851">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f36fd-852">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-852">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36fd-853">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-853">Az.Automation</span></span>
* <span data-ttu-id="f36fd-854">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-854">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f36fd-855">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-855">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f36fd-856">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="f36fd-856">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f36fd-857">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f36fd-857">Az.Cdn</span></span>
* <span data-ttu-id="f36fd-858">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-858">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-859">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-859">Az.Compute</span></span>
* <span data-ttu-id="f36fd-860">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-860">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36fd-861">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36fd-861">Az.DataFactory</span></span>
* <span data-ttu-id="f36fd-862">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f36fd-862">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f36fd-863">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f36fd-863">Az.LogicApp</span></span>
* <span data-ttu-id="f36fd-864">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="f36fd-864">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-865">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-865">Az.Network</span></span>
* <span data-ttu-id="f36fd-866">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-866">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-868">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-868">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f36fd-869">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="f36fd-869">SDK Update</span></span>
* <span data-ttu-id="f36fd-870">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="f36fd-870">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f36fd-871">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="f36fd-871">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-872">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-872">Az.Resources</span></span>
* <span data-ttu-id="f36fd-873">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-873">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f36fd-874">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f36fd-874">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f36fd-875">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-875">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f36fd-876">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f36fd-876">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f36fd-877">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-877">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f36fd-878">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f36fd-878">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-879">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-879">Az.Sql</span></span>
* <span data-ttu-id="f36fd-880">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="f36fd-880">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f36fd-881">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="f36fd-881">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-882">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-882">Az.Storage</span></span>
* <span data-ttu-id="f36fd-883">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f36fd-883">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f36fd-884">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-884">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f36fd-885">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-885">Az.AnalysisServices</span></span>
* <span data-ttu-id="f36fd-886">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-886">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36fd-887">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-887">Az.Automation</span></span>
* <span data-ttu-id="f36fd-888">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="f36fd-888">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f36fd-889">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-889">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f36fd-890">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="f36fd-890">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36fd-891">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-891">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36fd-892">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="f36fd-892">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-893">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-893">Az.Compute</span></span>
* <span data-ttu-id="f36fd-894">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-894">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f36fd-895">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="f36fd-895">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f36fd-896">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-896">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f36fd-897">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="f36fd-897">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-898">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-898">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36fd-899">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-899">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f36fd-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-900">Az.EventHub</span></span>
* <span data-ttu-id="f36fd-901">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="f36fd-901">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="f36fd-902">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36fd-902">Az.KeyVault</span></span>
* <span data-ttu-id="f36fd-903">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="f36fd-903">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f36fd-904">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f36fd-904">Az.LogicApp</span></span>
* <span data-ttu-id="f36fd-905">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="f36fd-905">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f36fd-906">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="f36fd-906">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f36fd-907">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-907">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f36fd-908">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f36fd-908">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f36fd-909">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f36fd-909">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f36fd-910">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f36fd-910">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f36fd-911">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f36fd-911">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f36fd-912">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-912">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f36fd-913">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36fd-913">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f36fd-914">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36fd-914">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f36fd-915">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36fd-915">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f36fd-916">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36fd-916">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f36fd-917">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="f36fd-917">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f36fd-918">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36fd-918">Az.Monitor</span></span>
* <span data-ttu-id="f36fd-919">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="f36fd-919">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-920">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-920">Az.Network</span></span>
* <span data-ttu-id="f36fd-921">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-921">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f36fd-922">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-922">Az.OperationalInsights</span></span>
* <span data-ttu-id="f36fd-923">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-923">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f36fd-924">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="f36fd-924">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="f36fd-925">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fd-925">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="f36fd-926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-926">Az.Resources</span></span>
* <span data-ttu-id="f36fd-927">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-927">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f36fd-928">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-928">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f36fd-929">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-929">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f36fd-930">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="f36fd-930">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-931">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-931">Az.Sql</span></span>
* <span data-ttu-id="f36fd-932">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-932">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f36fd-933">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="f36fd-933">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-934">Az.Websites</span></span>
* <span data-ttu-id="f36fd-935">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-935">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f36fd-936">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-936">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-937">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-937">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-938">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f36fd-938">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f36fd-939">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-939">Az.AnalysisServices</span></span>
<span data-ttu-id="f36fd-940">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="f36fd-940">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-941">Az.Compute</span></span>
* <span data-ttu-id="f36fd-942">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-942">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f36fd-943">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-943">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f36fd-944">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-944">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-945">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-945">Az.RecoveryServices</span></span>
<span data-ttu-id="f36fd-946">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="f36fd-946">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-947">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-947">Az.Resources</span></span>
* <span data-ttu-id="f36fd-948">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="f36fd-948">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="f36fd-949">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f36fd-949">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f36fd-950">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-950">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="f36fd-951">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f36fd-951">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-952">Az.Sql</span></span>
* <span data-ttu-id="f36fd-953">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f36fd-953">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f36fd-954">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-954">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f36fd-955">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="f36fd-955">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f36fd-956">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-956">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-957">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-957">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-958">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="f36fd-958">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f36fd-959">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-959">Az.AnalysisServices</span></span>
* <span data-ttu-id="f36fd-960">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="f36fd-960">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-961">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-961">Az.RecoveryServices</span></span>
* <span data-ttu-id="f36fd-962">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="f36fd-962">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f36fd-963">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-963">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-964">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-965">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="f36fd-965">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f36fd-966">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-966">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f36fd-967">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="f36fd-967">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f36fd-968">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f36fd-968">Az.Aks</span></span>
* <span data-ttu-id="f36fd-969">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-969">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f36fd-970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-970">Az.Automation</span></span>
* <span data-ttu-id="f36fd-971">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-971">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f36fd-972">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-972">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f36fd-973">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f36fd-973">Az.Cdn</span></span>
* <span data-ttu-id="f36fd-974">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-974">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-975">Az.Compute</span></span>
* <span data-ttu-id="f36fd-976">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-976">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f36fd-977">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f36fd-977">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f36fd-978">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="f36fd-978">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f36fd-979">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f36fd-979">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f36fd-980">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-980">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f36fd-981">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f36fd-981">Az.DataFactory</span></span>
* <span data-ttu-id="f36fd-982">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f36fd-982">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-983">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-983">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36fd-984">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-984">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f36fd-985">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f36fd-985">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f36fd-986">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-986">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f36fd-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-987">Az.IotHub</span></span>
* <span data-ttu-id="f36fd-988">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f36fd-988">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f36fd-989">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36fd-989">Az.KeyVault</span></span>
* <span data-ttu-id="f36fd-990">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-990">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-991">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-991">Az.Network</span></span>
* <span data-ttu-id="f36fd-992">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-992">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-993">Az.Resources</span></span>
* <span data-ttu-id="f36fd-994">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-994">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f36fd-995">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-995">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f36fd-996">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="f36fd-996">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f36fd-997">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-997">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f36fd-998">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-998">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f36fd-999">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-999">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f36fd-1000">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f36fd-1000">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f36fd-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36fd-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36fd-1002">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f36fd-1002">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f36fd-1003">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1003">Fix some error messages.</span></span>
* <span data-ttu-id="f36fd-1004">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1004">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f36fd-1005">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1005">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f36fd-1006">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f36fd-1006">Az.SignalR</span></span>
* <span data-ttu-id="f36fd-1007">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-1007">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-1008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-1008">Az.Sql</span></span>
* <span data-ttu-id="f36fd-1009">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-1009">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f36fd-1010">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="f36fd-1010">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f36fd-1011">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1011">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f36fd-1012">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="f36fd-1012">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-1013">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-1013">Az.Storage</span></span>
* <span data-ttu-id="f36fd-1014">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-1014">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f36fd-1015">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1015">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f36fd-1016">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f36fd-1016">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f36fd-1017">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f36fd-1017">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f36fd-1018">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f36fd-1018">Az.TrafficManager</span></span>
* <span data-ttu-id="f36fd-1019">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-1019">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-1020">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-1020">Az.Websites</span></span>
* <span data-ttu-id="f36fd-1021">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-1021">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f36fd-1022">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1022">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f36fd-1023">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="f36fd-1023">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f36fd-1024">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-1024">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f36fd-1025">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-1025">Az.Accounts</span></span>
* <span data-ttu-id="f36fd-1026">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f36fd-1026">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-1027">Az.Compute</span></span>
* <span data-ttu-id="f36fd-1028">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="f36fd-1028">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f36fd-1029">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-1029">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f36fd-1030">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1030">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-1031">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-1031">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36fd-1032">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1032">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f36fd-1033">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="f36fd-1033">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f36fd-1034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f36fd-1034">Az.EventGrid</span></span>
* <span data-ttu-id="f36fd-1035">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1035">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f36fd-1036">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="f36fd-1036">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f36fd-1037">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="f36fd-1037">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f36fd-1038">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="f36fd-1038">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f36fd-1039">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="f36fd-1039">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f36fd-1040">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1040">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f36fd-1041">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="f36fd-1041">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f36fd-1042">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="f36fd-1042">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f36fd-1043">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="f36fd-1043">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f36fd-1044">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1044">Dead letter endpoint.</span></span>
* <span data-ttu-id="f36fd-1045">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1045">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f36fd-1046">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1046">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f36fd-1047">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f36fd-1047">Az.IotHub</span></span>
* <span data-ttu-id="f36fd-1048">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="f36fd-1048">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f36fd-1049">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f36fd-1049">Az.LogicApp</span></span>
* <span data-ttu-id="f36fd-1050">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="f36fd-1050">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-1051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-1051">Az.Resources</span></span>
* <span data-ttu-id="f36fd-1052">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1052">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f36fd-1053">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f36fd-1053">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f36fd-1054">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="f36fd-1054">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f36fd-1055">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-1055">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f36fd-1056">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="f36fd-1056">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f36fd-1057">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f36fd-1057">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f36fd-1058">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f36fd-1058">Az.SignalR</span></span>
* <span data-ttu-id="f36fd-1059">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1059">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-1060">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-1060">Az.Sql</span></span>
* <span data-ttu-id="f36fd-1061">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1061">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f36fd-1062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-1062">Az.Storage</span></span>
* <span data-ttu-id="f36fd-1063">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="f36fd-1063">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f36fd-1064">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f36fd-1064">New-AzStorageContext</span></span>
* <span data-ttu-id="f36fd-1065">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="f36fd-1065">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f36fd-1066">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f36fd-1066">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-1067">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-1067">Az.Websites</span></span>
* <span data-ttu-id="f36fd-1068">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="f36fd-1068">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f36fd-1069">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1069">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f36fd-1070">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-1070">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f36fd-1071">一般</span><span class="sxs-lookup"><span data-stu-id="f36fd-1071">General</span></span>

- <span data-ttu-id="f36fd-1072">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="f36fd-1072">General Availability of Az Module</span></span>
- <span data-ttu-id="f36fd-1073">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="f36fd-1073">Online help for each module</span></span>
- <span data-ttu-id="f36fd-1074">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1074">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f36fd-1075">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1075">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f36fd-1076">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-1076">Az.Accounts</span></span>
- <span data-ttu-id="f36fd-1077">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="f36fd-1077">Changed from Az.Profile</span></span>
- <span data-ttu-id="f36fd-1078">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="f36fd-1078">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f36fd-1079">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f36fd-1079">Az.ApiManagement</span></span>
- <span data-ttu-id="f36fd-1080">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="f36fd-1080">Fixes for #7002</span></span>
- <span data-ttu-id="f36fd-1081">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1081">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f36fd-1082">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f36fd-1082">Az.Batch</span></span>
- <span data-ttu-id="f36fd-1083">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1083">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f36fd-1084">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1084">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f36fd-1085">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1085">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f36fd-1086">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f36fd-1086">Az.Billing</span></span>
- <span data-ttu-id="f36fd-1087">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1087">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f36fd-1088">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-1088">Az.CognitivServices</span></span>
- <span data-ttu-id="f36fd-1089">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="f36fd-1089">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f36fd-1090">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="f36fd-1090">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f36fd-1091">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f36fd-1091">Az.ContainerInstance</span></span>
- <span data-ttu-id="f36fd-1092">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-1092">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f36fd-1093">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f36fd-1093">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f36fd-1094">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1094">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-1095">Az.DataLakeStore</span></span>
- <span data-ttu-id="f36fd-1096">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1096">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f36fd-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f36fd-1097">Az.Monitor</span></span>
- <span data-ttu-id="f36fd-1098">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1098">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f36fd-1099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f36fd-1099">Az.KeyVault</span></span>
- <span data-ttu-id="f36fd-1100">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="f36fd-1100">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f36fd-1101">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f36fd-1101">Az.MachineLearning</span></span>
- <span data-ttu-id="f36fd-1102">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1102">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f36fd-1103">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f36fd-1103">Az.Media</span></span>
- <span data-ttu-id="f36fd-1104">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="f36fd-1104">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f36fd-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-1105">Az.Network</span></span>
<span data-ttu-id="f36fd-1106">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-1106">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f36fd-1107">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="f36fd-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="f36fd-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1108">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36fd-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1109">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36fd-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1110">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36fd-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1111">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36fd-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1112">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f36fd-1113">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-1113">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f36fd-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1114">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f36fd-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36fd-1115">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f36fd-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1116">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f36fd-1117">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f36fd-1117">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f36fd-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-1118">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f36fd-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f36fd-1119">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f36fd-1120">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-1120">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f36fd-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-1121">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f36fd-1122">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1122">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f36fd-1123">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1123">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f36fd-1124">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f36fd-1124">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f36fd-1125">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f36fd-1125">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f36fd-1126">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f36fd-1126">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f36fd-1127">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1127">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f36fd-1128">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1128">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f36fd-1129">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-1129">Az.OperationalInsights</span></span>
- <span data-ttu-id="f36fd-1130">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1130">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f36fd-1131">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f36fd-1131">Az.Profile</span></span>
- <span data-ttu-id="f36fd-1132">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f36fd-1132">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-1133">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-1133">Az.RecoveryServices</span></span>
- <span data-ttu-id="f36fd-1134">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f36fd-1135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-1135">Az.Resources</span></span>
- <span data-ttu-id="f36fd-1136">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1136">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f36fd-1137">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36fd-1137">Az.ServiceFabric</span></span>
- <span data-ttu-id="f36fd-1138">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="f36fd-1138">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f36fd-1139">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1139">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f36fd-1140">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f36fd-1140">Az.SIgnalR</span></span>
- <span data-ttu-id="f36fd-1141">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="f36fd-1141">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f36fd-1142">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-1142">Az.Sql</span></span>
- <span data-ttu-id="f36fd-1143">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="f36fd-1143">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f36fd-1144">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-1144">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f36fd-1145">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1145">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f36fd-1146">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-1146">Az.Storage</span></span>
- <span data-ttu-id="f36fd-1147">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f36fd-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-1148">Az.Websites</span></span>
- <span data-ttu-id="f36fd-1149">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f36fd-1150">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-1150">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f36fd-1151">一般</span><span class="sxs-lookup"><span data-stu-id="f36fd-1151">General</span></span>

* <span data-ttu-id="f36fd-1152">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="f36fd-1152">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f36fd-1153">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-1153">Az.Compute</span></span>

* <span data-ttu-id="f36fd-1154">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1154">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-1155">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-1155">Az.DataLakeStore</span></span>

* <span data-ttu-id="f36fd-1156">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="f36fd-1156">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f36fd-1157">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f36fd-1157">Az.FrontDoor</span></span>

* <span data-ttu-id="f36fd-1158">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="f36fd-1158">Fixed some broken links</span></span>
    - <span data-ttu-id="f36fd-1159">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1159">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f36fd-1160">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1160">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f36fd-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-1161">Az.RecoveryServices</span></span>

* <span data-ttu-id="f36fd-1162">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1162">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f36fd-1163">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1163">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f36fd-1164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-1164">Az.Resources</span></span>

* <span data-ttu-id="f36fd-1165">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f36fd-1165">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f36fd-1166">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1166">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f36fd-1167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-1167">Az.Sql</span></span>

* <span data-ttu-id="f36fd-1168">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="f36fd-1168">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f36fd-1169">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1169">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f36fd-1170">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1170">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f36fd-1171">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-1171">Az.Storage</span></span>

* <span data-ttu-id="f36fd-1172">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="f36fd-1172">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f36fd-1173">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="f36fd-1173">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f36fd-1174">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f36fd-1174">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f36fd-1175">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="f36fd-1175">Support Static Website configuration</span></span>
    - <span data-ttu-id="f36fd-1176">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f36fd-1176">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f36fd-1177">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f36fd-1177">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f36fd-1178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-1178">Az.Websites</span></span>

* <span data-ttu-id="f36fd-1179">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f36fd-1179">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="f36fd-1180">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1180">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f36fd-1181">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1181">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f36fd-1182">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-1182">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f36fd-1183">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f36fd-1183">Az.ApiManagement</span></span>
* <span data-ttu-id="f36fd-1184">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="f36fd-1184">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f36fd-1185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f36fd-1185">Az.Automation</span></span>
* <span data-ttu-id="f36fd-1186">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1186">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f36fd-1187">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1187">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f36fd-1188">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1188">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f36fd-1189">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1189">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f36fd-1190">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="f36fd-1190">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f36fd-1191">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-1191">Az.Compute</span></span>
* <span data-ttu-id="f36fd-1192">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1192">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f36fd-1193">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="f36fd-1193">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f36fd-1194">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f36fd-1194">Az.ContainerInstance</span></span>
* <span data-ttu-id="f36fd-1195">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="f36fd-1195">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f36fd-1196">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f36fd-1196">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f36fd-1197">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="f36fd-1197">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f36fd-1198">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-1198">Az.Network</span></span>
* <span data-ttu-id="f36fd-1199">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="f36fd-1199">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f36fd-1200">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="f36fd-1200">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f36fd-1201">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1201">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="f36fd-1202">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1202">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f36fd-1203">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f36fd-1203">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f36fd-1204">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1204">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f36fd-1205">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1205">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f36fd-1206">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f36fd-1206">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f36fd-1207">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-1207">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f36fd-1208">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="f36fd-1208">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f36fd-1209">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f36fd-1209">Az.Relay</span></span>
* <span data-ttu-id="f36fd-1210">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1210">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f36fd-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-1211">Az.Resources</span></span>
* <span data-ttu-id="f36fd-1212">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="f36fd-1212">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f36fd-1213">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="f36fd-1213">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f36fd-1214">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="f36fd-1214">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f36fd-1215">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36fd-1215">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36fd-1216">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="f36fd-1216">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f36fd-1217">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-1217">Az.Sql</span></span>
* <span data-ttu-id="f36fd-1218">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1218">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f36fd-1219">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f36fd-1219">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f36fd-1220">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f36fd-1220">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f36fd-1221">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f36fd-1221">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f36fd-1222">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f36fd-1222">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f36fd-1223">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f36fd-1223">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f36fd-1224">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f36fd-1224">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f36fd-1225">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f36fd-1225">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f36fd-1226">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f36fd-1226">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f36fd-1227">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1227">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f36fd-1228">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1228">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f36fd-1229">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1229">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f36fd-1230">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1230">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f36fd-1231">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1231">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f36fd-1232">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1232">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f36fd-1233">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1233">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f36fd-1234">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1234">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f36fd-1235">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-1235">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f36fd-1236">一般</span><span class="sxs-lookup"><span data-stu-id="f36fd-1236">General</span></span>
* <span data-ttu-id="f36fd-1237">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="f36fd-1237">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f36fd-1238">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f36fd-1238">Az.Profile</span></span>
* <span data-ttu-id="f36fd-1239">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f36fd-1239">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f36fd-1240">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="f36fd-1240">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f36fd-1241">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="f36fd-1241">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f36fd-1242">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="f36fd-1242">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f36fd-1243">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1243">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f36fd-1244">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1244">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f36fd-1245">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1245">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f36fd-1246">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-1246">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36fd-1247">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1247">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-1248">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-1248">Az.Compute</span></span>
* <span data-ttu-id="f36fd-1249">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1249">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f36fd-1250">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f36fd-1250">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f36fd-1251">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1251">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-1252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-1252">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36fd-1253">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1253">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f36fd-1254">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1254">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f36fd-1255">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f36fd-1255">Az.Insights</span></span>
* <span data-ttu-id="f36fd-1256">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="f36fd-1256">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f36fd-1257">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1257">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f36fd-1258">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="f36fd-1258">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f36fd-1259">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="f36fd-1259">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-1260">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-1260">Az.Network</span></span>
* <span data-ttu-id="f36fd-1261">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="f36fd-1261">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f36fd-1262">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f36fd-1262">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f36fd-1263">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f36fd-1263">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f36fd-1264">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f36fd-1264">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f36fd-1265">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f36fd-1265">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f36fd-1266">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f36fd-1266">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f36fd-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f36fd-1267">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f36fd-1268">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f36fd-1268">Az.PolicyInsights</span></span>
* <span data-ttu-id="f36fd-1269">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1269">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-1270">Az.Resources</span></span>
* <span data-ttu-id="f36fd-1271">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f36fd-1271">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f36fd-1272">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="f36fd-1272">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f36fd-1273">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f36fd-1273">Az.ServiceBus</span></span>
* <span data-ttu-id="f36fd-1274">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1274">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f36fd-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f36fd-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="f36fd-1276">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1276">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f36fd-1277">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="f36fd-1277">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f36fd-1278">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1278">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f36fd-1279">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1279">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f36fd-1280">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1280">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f36fd-1281">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-1281">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f36fd-1282">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f36fd-1282">Az.Profile</span></span>
* <span data-ttu-id="f36fd-1283">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1283">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f36fd-1284">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f36fd-1284">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-1285">Az.Compute</span></span>
* <span data-ttu-id="f36fd-1286">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="f36fd-1286">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f36fd-1287">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1287">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f36fd-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f36fd-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="f36fd-1289">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="f36fd-1289">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f36fd-1290">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1290">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f36fd-1291">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1291">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f36fd-1292">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1292">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f36fd-1293">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1293">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-1294">Az.Network</span></span>
* <span data-ttu-id="f36fd-1295">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1295">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f36fd-1296">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1296">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-1297">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-1297">Az.Resources</span></span>
* <span data-ttu-id="f36fd-1298">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1298">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f36fd-1299">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1299">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f36fd-1300">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-1300">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f36fd-1301">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f36fd-1301">Azure.Storage</span></span>
* <span data-ttu-id="f36fd-1302">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1302">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f36fd-1303">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f36fd-1303">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f36fd-1304">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f36fd-1304">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f36fd-1305">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1305">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f36fd-1306">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f36fd-1306">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="f36fd-1307">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f36fd-1307">Az.CognitiveServices</span></span>
* <span data-ttu-id="f36fd-1308">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1308">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f36fd-1309">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f36fd-1309">Az.Compute</span></span>
* <span data-ttu-id="f36fd-1310">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="f36fd-1310">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f36fd-1311">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1311">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f36fd-1312">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="f36fd-1312">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f36fd-1313">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f36fd-1313">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f36fd-1314">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1314">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f36fd-1315">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f36fd-1315">Az.Network</span></span>
* <span data-ttu-id="f36fd-1316">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1316">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f36fd-1317">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1317">new cmdlets added</span></span>
    - <span data-ttu-id="f36fd-1318">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36fd-1318">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f36fd-1319">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36fd-1319">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f36fd-1320">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36fd-1320">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f36fd-1321">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f36fd-1321">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f36fd-1322">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-1322">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f36fd-1323">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f36fd-1323">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f36fd-1324">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="f36fd-1324">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f36fd-1325">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1325">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f36fd-1326">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f36fd-1326">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f36fd-1327">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f36fd-1327">Az.RedisCache</span></span>
* <span data-ttu-id="f36fd-1328">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="f36fd-1328">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f36fd-1329">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="f36fd-1329">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f36fd-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f36fd-1330">Az.Resources</span></span>
* <span data-ttu-id="f36fd-1331">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f36fd-1331">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f36fd-1332">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="f36fd-1332">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f36fd-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f36fd-1333">Az.Sql</span></span>
* <span data-ttu-id="f36fd-1334">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="f36fd-1334">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f36fd-1335">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f36fd-1335">Az.Websites</span></span>
* <span data-ttu-id="f36fd-1336">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="f36fd-1336">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f36fd-1337">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="f36fd-1337">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f36fd-1338">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="f36fd-1338">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f36fd-1339">初始版本</span><span class="sxs-lookup"><span data-stu-id="f36fd-1339">Initial Release</span></span>