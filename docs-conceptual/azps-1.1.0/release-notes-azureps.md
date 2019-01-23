---
ms.openlocfilehash: 179d22fa065944695e4769f2698e3cabc7666b04
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/16/2019
ms.locfileid: "54341889"
---
## <a name="110---january-2019"></a><span data-ttu-id="9c1cb-101">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="9c1cb-101">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="9c1cb-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9c1cb-102">Az.Accounts</span></span>
* <span data-ttu-id="9c1cb-103">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="9c1cb-103">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9c1cb-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9c1cb-104">Az.Compute</span></span>
* <span data-ttu-id="9c1cb-105">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="9c1cb-105">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="9c1cb-106">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="9c1cb-106">Updated the description of ID in help files</span></span>
* <span data-ttu-id="9c1cb-107">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-107">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9c1cb-108">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9c1cb-108">Az.DataLakeStore</span></span>
* <span data-ttu-id="9c1cb-109">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-109">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="9c1cb-110">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="9c1cb-110">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="9c1cb-111">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9c1cb-111">Az.EventGrid</span></span>
* <span data-ttu-id="9c1cb-112">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-112">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="9c1cb-113">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="9c1cb-113">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="9c1cb-114">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="9c1cb-114">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9c1cb-115">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="9c1cb-115">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9c1cb-116">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="9c1cb-116">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9c1cb-117">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-117">Dead letter endpoint.</span></span>
    - <span data-ttu-id="9c1cb-118">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="9c1cb-118">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="9c1cb-119">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="9c1cb-119">Event Time-To-Live,</span></span>
        - <span data-ttu-id="9c1cb-120">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="9c1cb-120">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="9c1cb-121">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-121">Dead letter endpoint.</span></span>
* <span data-ttu-id="9c1cb-122">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-122">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="9c1cb-123">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-123">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="9c1cb-124">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="9c1cb-124">Az.IotHub</span></span>
* <span data-ttu-id="9c1cb-125">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="9c1cb-125">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="9c1cb-126">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9c1cb-126">Az.LogicApp</span></span>
* <span data-ttu-id="9c1cb-127">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="9c1cb-127">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="9c1cb-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9c1cb-128">Az.Resources</span></span>
* <span data-ttu-id="9c1cb-129">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-129">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="9c1cb-130">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="9c1cb-130">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="9c1cb-131">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="9c1cb-131">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9c1cb-132">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="9c1cb-132">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="9c1cb-133">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="9c1cb-133">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="9c1cb-134">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="9c1cb-134">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="9c1cb-135">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="9c1cb-135">Az.SignalR</span></span>
* <span data-ttu-id="9c1cb-136">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-136">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="9c1cb-137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9c1cb-137">Az.Sql</span></span>
* <span data-ttu-id="9c1cb-138">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-138">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="9c1cb-139">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9c1cb-139">Az.Storage</span></span>
* <span data-ttu-id="9c1cb-140">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="9c1cb-140">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="9c1cb-141">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9c1cb-141">New-AzStorageContext</span></span>
* <span data-ttu-id="9c1cb-142">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="9c1cb-142">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="9c1cb-143">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9c1cb-143">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9c1cb-144">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9c1cb-144">Az.Websites</span></span>
* <span data-ttu-id="9c1cb-145">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="9c1cb-145">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="9c1cb-146">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-146">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="9c1cb-147">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="9c1cb-147">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="9c1cb-148">一般</span><span class="sxs-lookup"><span data-stu-id="9c1cb-148">General</span></span>

- <span data-ttu-id="9c1cb-149">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="9c1cb-149">General Availability of Az Module</span></span>
- <span data-ttu-id="9c1cb-150">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="9c1cb-150">Online help for each module</span></span>
- <span data-ttu-id="9c1cb-151">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-151">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="9c1cb-152">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-152">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="9c1cb-153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9c1cb-153">Az.Accounts</span></span>
- <span data-ttu-id="9c1cb-154">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="9c1cb-154">Changed from Az.Profile</span></span>
- <span data-ttu-id="9c1cb-155">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="9c1cb-155">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9c1cb-156">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c1cb-156">Az.ApiManagement</span></span>
- <span data-ttu-id="9c1cb-157">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="9c1cb-157">Fixes for #7002</span></span>
- <span data-ttu-id="9c1cb-158">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-158">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="9c1cb-159">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="9c1cb-159">Az.Batch</span></span>
- <span data-ttu-id="9c1cb-160">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-160">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="9c1cb-161">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-161">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="9c1cb-162">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-162">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="9c1cb-163">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="9c1cb-163">Az.Billing</span></span>
- <span data-ttu-id="9c1cb-164">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-164">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="9c1cb-165">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="9c1cb-165">Az.CognitivServices</span></span>
- <span data-ttu-id="9c1cb-166">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="9c1cb-166">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="9c1cb-167">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="9c1cb-167">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9c1cb-168">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9c1cb-168">Az.ContainerInstance</span></span>
- <span data-ttu-id="9c1cb-169">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="9c1cb-169">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="9c1cb-170">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9c1cb-170">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="9c1cb-171">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-171">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9c1cb-172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9c1cb-172">Az.DataLakeStore</span></span>
- <span data-ttu-id="9c1cb-173">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-173">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="9c1cb-174">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9c1cb-174">Az.Monitor</span></span>
- <span data-ttu-id="9c1cb-175">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-175">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="9c1cb-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9c1cb-176">Az.KeyVault</span></span>
- <span data-ttu-id="9c1cb-177">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="9c1cb-177">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="9c1cb-178">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9c1cb-178">Az.MachineLearning</span></span>
- <span data-ttu-id="9c1cb-179">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-179">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="9c1cb-180">Az.Media</span><span class="sxs-lookup"><span data-stu-id="9c1cb-180">Az.Media</span></span>
- <span data-ttu-id="9c1cb-181">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="9c1cb-181">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9c1cb-182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9c1cb-182">Az.Network</span></span>
<span data-ttu-id="9c1cb-183">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="9c1cb-183">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="9c1cb-184">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9c1cb-184">New cmdlets added:</span></span>
        - <span data-ttu-id="9c1cb-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-185">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9c1cb-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-186">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9c1cb-187">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-187">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9c1cb-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-188">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9c1cb-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-189">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="9c1cb-190">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9c1cb-190">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="9c1cb-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-191">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="9c1cb-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c1cb-192">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="9c1cb-193">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-193">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="9c1cb-194">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c1cb-194">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="9c1cb-195">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c1cb-195">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9c1cb-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c1cb-196">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="9c1cb-197">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9c1cb-197">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="9c1cb-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9c1cb-198">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="9c1cb-199">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-199">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="9c1cb-200">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-200">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="9c1cb-201">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9c1cb-201">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9c1cb-202">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9c1cb-202">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="9c1cb-203">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9c1cb-203">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="9c1cb-204">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-204">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="9c1cb-205">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-205">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="9c1cb-206">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9c1cb-206">Az.OperationalInsights</span></span>
- <span data-ttu-id="9c1cb-207">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-207">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="9c1cb-208">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9c1cb-208">Az.Profile</span></span>
- <span data-ttu-id="9c1cb-209">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9c1cb-209">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9c1cb-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9c1cb-210">Az.RecoveryServices</span></span>
- <span data-ttu-id="9c1cb-211">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-211">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="9c1cb-212">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9c1cb-212">Az.Resources</span></span>
- <span data-ttu-id="9c1cb-213">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-213">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9c1cb-214">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9c1cb-214">Az.ServiceFabric</span></span>
- <span data-ttu-id="9c1cb-215">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="9c1cb-215">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="9c1cb-216">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-216">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="9c1cb-217">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="9c1cb-217">Az.SIgnalR</span></span>
- <span data-ttu-id="9c1cb-218">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="9c1cb-218">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="9c1cb-219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9c1cb-219">Az.Sql</span></span>
- <span data-ttu-id="9c1cb-220">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="9c1cb-220">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="9c1cb-221">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="9c1cb-221">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="9c1cb-222">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-222">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="9c1cb-223">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9c1cb-223">Az.Storage</span></span>
- <span data-ttu-id="9c1cb-224">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-224">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9c1cb-225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9c1cb-225">Az.Websites</span></span>
- <span data-ttu-id="9c1cb-226">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-226">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="9c1cb-227">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="9c1cb-227">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="9c1cb-228">一般</span><span class="sxs-lookup"><span data-stu-id="9c1cb-228">General</span></span>

* <span data-ttu-id="9c1cb-229">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="9c1cb-229">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="9c1cb-230">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9c1cb-230">Az.Compute</span></span>

* <span data-ttu-id="9c1cb-231">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-231">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="9c1cb-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9c1cb-232">Az.DataLakeStore</span></span>

* <span data-ttu-id="9c1cb-233">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="9c1cb-233">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="9c1cb-234">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9c1cb-234">Az.FrontDoor</span></span>

* <span data-ttu-id="9c1cb-235">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="9c1cb-235">Fixed some broken links</span></span>
    - <span data-ttu-id="9c1cb-236">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-236">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="9c1cb-237">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-237">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="9c1cb-238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9c1cb-238">Az.RecoveryServices</span></span>

* <span data-ttu-id="9c1cb-239">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-239">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="9c1cb-240">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-240">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="9c1cb-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9c1cb-241">Az.Resources</span></span>

* <span data-ttu-id="9c1cb-242">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="9c1cb-242">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="9c1cb-243">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-243">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="9c1cb-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9c1cb-244">Az.Sql</span></span>

* <span data-ttu-id="9c1cb-245">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="9c1cb-245">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="9c1cb-246">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-246">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="9c1cb-247">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-247">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="9c1cb-248">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9c1cb-248">Az.Storage</span></span>

* <span data-ttu-id="9c1cb-249">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="9c1cb-249">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="9c1cb-250">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="9c1cb-250">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="9c1cb-251">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9c1cb-251">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9c1cb-252">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="9c1cb-252">Support Static Website configuration</span></span>
    - <span data-ttu-id="9c1cb-253">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9c1cb-253">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="9c1cb-254">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="9c1cb-254">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="9c1cb-255">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9c1cb-255">Az.Websites</span></span>

* <span data-ttu-id="9c1cb-256">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9c1cb-256">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="9c1cb-257">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-257">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="9c1cb-258">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-258">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="9c1cb-259">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="9c1cb-259">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="9c1cb-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c1cb-260">Az.ApiManagement</span></span>
* <span data-ttu-id="9c1cb-261">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="9c1cb-261">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="9c1cb-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="9c1cb-262">Az.Automation</span></span>
* <span data-ttu-id="9c1cb-263">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-263">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="9c1cb-264">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-264">Added Update Management cmdlets</span></span>
* <span data-ttu-id="9c1cb-265">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-265">Added Source Control cmdlets</span></span>
* <span data-ttu-id="9c1cb-266">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-266">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="9c1cb-267">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="9c1cb-267">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="9c1cb-268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9c1cb-268">Az.Compute</span></span>
* <span data-ttu-id="9c1cb-269">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-269">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="9c1cb-270">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="9c1cb-270">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="9c1cb-271">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9c1cb-271">Az.ContainerInstance</span></span>
* <span data-ttu-id="9c1cb-272">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="9c1cb-272">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="9c1cb-273">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="9c1cb-273">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="9c1cb-274">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="9c1cb-274">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="9c1cb-275">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9c1cb-275">Az.Network</span></span>
* <span data-ttu-id="9c1cb-276">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9c1cb-276">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="9c1cb-277">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="9c1cb-277">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="9c1cb-278">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-278">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="9c1cb-279">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-279">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="9c1cb-280">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9c1cb-280">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9c1cb-281">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-281">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="9c1cb-282">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-282">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="9c1cb-283">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9c1cb-283">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="9c1cb-284">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="9c1cb-284">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="9c1cb-285">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="9c1cb-285">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="9c1cb-286">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="9c1cb-286">Az.Relay</span></span>
* <span data-ttu-id="9c1cb-287">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-287">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="9c1cb-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9c1cb-288">Az.Resources</span></span>
* <span data-ttu-id="9c1cb-289">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="9c1cb-289">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="9c1cb-290">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="9c1cb-290">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="9c1cb-291">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="9c1cb-291">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="9c1cb-292">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9c1cb-292">Az.ServiceFabric</span></span>
* <span data-ttu-id="9c1cb-293">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="9c1cb-293">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="9c1cb-294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9c1cb-294">Az.Sql</span></span>
* <span data-ttu-id="9c1cb-295">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-295">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="9c1cb-296">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9c1cb-296">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9c1cb-297">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9c1cb-297">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9c1cb-298">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9c1cb-298">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9c1cb-299">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9c1cb-299">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="9c1cb-300">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9c1cb-300">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9c1cb-301">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9c1cb-301">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9c1cb-302">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9c1cb-302">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="9c1cb-303">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="9c1cb-303">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="9c1cb-304">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-304">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="9c1cb-305">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-305">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="9c1cb-306">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-306">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="9c1cb-307">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-307">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9c1cb-308">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-308">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="9c1cb-309">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-309">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="9c1cb-310">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-310">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="9c1cb-311">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-311">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="9c1cb-312">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="9c1cb-312">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9c1cb-313">一般</span><span class="sxs-lookup"><span data-stu-id="9c1cb-313">General</span></span>
* <span data-ttu-id="9c1cb-314">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="9c1cb-314">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="9c1cb-315">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9c1cb-315">Az.Profile</span></span>
* <span data-ttu-id="9c1cb-316">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9c1cb-316">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="9c1cb-317">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="9c1cb-317">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="9c1cb-318">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="9c1cb-318">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="9c1cb-319">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="9c1cb-319">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="9c1cb-320">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-320">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="9c1cb-321">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-321">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="9c1cb-322">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-322">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="9c1cb-323">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9c1cb-323">Az.CognitiveServices</span></span>
* <span data-ttu-id="9c1cb-324">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-324">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9c1cb-325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9c1cb-325">Az.Compute</span></span>
* <span data-ttu-id="9c1cb-326">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-326">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="9c1cb-327">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="9c1cb-327">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="9c1cb-328">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-328">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9c1cb-329">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9c1cb-329">Az.DataLakeStore</span></span>
* <span data-ttu-id="9c1cb-330">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-330">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="9c1cb-331">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-331">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="9c1cb-332">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="9c1cb-332">Az.Insights</span></span>
* <span data-ttu-id="9c1cb-333">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="9c1cb-333">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="9c1cb-334">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-334">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="9c1cb-335">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="9c1cb-335">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="9c1cb-336">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="9c1cb-336">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9c1cb-337">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9c1cb-337">Az.Network</span></span>
* <span data-ttu-id="9c1cb-338">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="9c1cb-338">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="9c1cb-339">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="9c1cb-339">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="9c1cb-340">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="9c1cb-340">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="9c1cb-341">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9c1cb-341">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="9c1cb-342">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="9c1cb-342">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="9c1cb-343">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="9c1cb-343">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="9c1cb-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9c1cb-344">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="9c1cb-345">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9c1cb-345">Az.PolicyInsights</span></span>
* <span data-ttu-id="9c1cb-346">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-346">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="9c1cb-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9c1cb-347">Az.Resources</span></span>
* <span data-ttu-id="9c1cb-348">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="9c1cb-348">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="9c1cb-349">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="9c1cb-349">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="9c1cb-350">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9c1cb-350">Az.ServiceBus</span></span>
* <span data-ttu-id="9c1cb-351">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-351">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="9c1cb-352">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9c1cb-352">Az.ServiceFabric</span></span>
* <span data-ttu-id="9c1cb-353">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-353">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="9c1cb-354">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="9c1cb-354">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="9c1cb-355">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-355">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="9c1cb-356">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-356">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="9c1cb-357">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-357">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="9c1cb-358">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="9c1cb-358">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="9c1cb-359">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="9c1cb-359">Az.Profile</span></span>
* <span data-ttu-id="9c1cb-360">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-360">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="9c1cb-361">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="9c1cb-361">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9c1cb-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9c1cb-362">Az.Compute</span></span>
* <span data-ttu-id="9c1cb-363">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="9c1cb-363">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="9c1cb-364">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-364">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="9c1cb-365">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9c1cb-365">Az.DataLakeStore</span></span>
* <span data-ttu-id="9c1cb-366">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="9c1cb-366">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="9c1cb-367">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-367">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="9c1cb-368">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-368">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9c1cb-369">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-369">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="9c1cb-370">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-370">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9c1cb-371">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9c1cb-371">Az.Network</span></span>
* <span data-ttu-id="9c1cb-372">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-372">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="9c1cb-373">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-373">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="9c1cb-374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9c1cb-374">Az.Resources</span></span>
* <span data-ttu-id="9c1cb-375">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-375">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="9c1cb-376">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-376">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="9c1cb-377">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="9c1cb-377">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="9c1cb-378">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9c1cb-378">Azure.Storage</span></span>
* <span data-ttu-id="9c1cb-379">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-379">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="9c1cb-380">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="9c1cb-380">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="9c1cb-381">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9c1cb-381">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="9c1cb-382">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-382">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="9c1cb-383">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="9c1cb-383">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="9c1cb-384">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9c1cb-384">Az.CognitiveServices</span></span>
* <span data-ttu-id="9c1cb-385">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-385">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="9c1cb-386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="9c1cb-386">Az.Compute</span></span>
* <span data-ttu-id="9c1cb-387">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="9c1cb-387">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="9c1cb-388">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-388">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="9c1cb-389">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="9c1cb-389">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="9c1cb-390">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9c1cb-390">Az.DataFactoryV2</span></span>
* <span data-ttu-id="9c1cb-391">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-391">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="9c1cb-392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="9c1cb-392">Az.Network</span></span>
* <span data-ttu-id="9c1cb-393">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-393">Added NetworkProfile functionality.</span></span> <span data-ttu-id="9c1cb-394">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-394">new cmdlets added</span></span>
    - <span data-ttu-id="9c1cb-395">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9c1cb-395">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="9c1cb-396">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9c1cb-396">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="9c1cb-397">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9c1cb-397">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="9c1cb-398">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="9c1cb-398">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="9c1cb-399">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="9c1cb-399">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="9c1cb-400">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="9c1cb-400">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="9c1cb-401">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="9c1cb-401">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="9c1cb-402">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-402">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="9c1cb-403">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9c1cb-403">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="9c1cb-404">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9c1cb-404">Az.RedisCache</span></span>
* <span data-ttu-id="9c1cb-405">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="9c1cb-405">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="9c1cb-406">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="9c1cb-406">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="9c1cb-407">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9c1cb-407">Az.Resources</span></span>
* <span data-ttu-id="9c1cb-408">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9c1cb-408">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="9c1cb-409">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="9c1cb-409">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="9c1cb-410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="9c1cb-410">Az.Sql</span></span>
* <span data-ttu-id="9c1cb-411">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="9c1cb-411">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="9c1cb-412">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="9c1cb-412">Az.Websites</span></span>
* <span data-ttu-id="9c1cb-413">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="9c1cb-413">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="9c1cb-414">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="9c1cb-414">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="9c1cb-415">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="9c1cb-415">0.2.0 - September 2018</span></span>
 <span data-ttu-id="9c1cb-416">初始版本</span><span class="sxs-lookup"><span data-stu-id="9c1cb-416">Initial Release</span></span>