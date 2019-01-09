## <a name="100---december-2018"></a><span data-ttu-id="c685f-101">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="c685f-101">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="c685f-102">一般</span><span class="sxs-lookup"><span data-stu-id="c685f-102">General</span></span>

- <span data-ttu-id="c685f-103">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="c685f-103">General Availability of Az Module</span></span>
- <span data-ttu-id="c685f-104">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="c685f-104">Online help for each module</span></span>
- <span data-ttu-id="c685f-105">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="c685f-105">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="c685f-106">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-106">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="c685f-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c685f-107">Az.Accounts</span></span>
- <span data-ttu-id="c685f-108">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="c685f-108">Changed from Az.Profile</span></span>
- <span data-ttu-id="c685f-109">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="c685f-109">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c685f-110">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c685f-110">Az.ApiManagement</span></span>
- <span data-ttu-id="c685f-111">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="c685f-111">Fixes for #7002</span></span>
- <span data-ttu-id="c685f-112">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-112">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="c685f-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="c685f-113">Az.Batch</span></span>
- <span data-ttu-id="c685f-114">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="c685f-114">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="c685f-115">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="c685f-115">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="c685f-116">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-116">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="c685f-117">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="c685f-117">Az.Billing</span></span>
- <span data-ttu-id="c685f-118">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-118">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="c685f-119">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="c685f-119">Az.CognitivServices</span></span>
- <span data-ttu-id="c685f-120">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="c685f-120">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="c685f-121">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="c685f-121">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c685f-122">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c685f-122">Az.ContainerInstance</span></span>
- <span data-ttu-id="c685f-123">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="c685f-123">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="c685f-124">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c685f-124">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="c685f-125">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-125">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c685f-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c685f-126">Az.DataLakeStore</span></span>
- <span data-ttu-id="c685f-127">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-127">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="c685f-128">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="c685f-128">Az.Monitor</span></span>
- <span data-ttu-id="c685f-129">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-129">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="c685f-130">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c685f-130">Az.KeyVault</span></span>
- <span data-ttu-id="c685f-131">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="c685f-131">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="c685f-132">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c685f-132">Az.MachineLearning</span></span>
- <span data-ttu-id="c685f-133">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-133">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="c685f-134">Az.Media</span><span class="sxs-lookup"><span data-stu-id="c685f-134">Az.Media</span></span>
- <span data-ttu-id="c685f-135">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="c685f-135">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c685f-136">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c685f-136">Az.Network</span></span>
<span data-ttu-id="c685f-137">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="c685f-137">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="c685f-138">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c685f-138">New cmdlets added:</span></span>
        - <span data-ttu-id="c685f-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c685f-139">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c685f-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c685f-140">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c685f-141">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c685f-141">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c685f-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c685f-142">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c685f-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c685f-143">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="c685f-144">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="c685f-144">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="c685f-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="c685f-145">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="c685f-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="c685f-146">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="c685f-147">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c685f-147">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="c685f-148">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c685f-148">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="c685f-149">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c685f-149">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c685f-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c685f-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="c685f-151">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c685f-151">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="c685f-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c685f-152">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="c685f-153">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="c685f-153">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="c685f-154">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-154">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="c685f-155">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c685f-155">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c685f-156">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c685f-156">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="c685f-157">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c685f-157">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="c685f-158">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-158">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="c685f-159">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-159">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="c685f-160">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c685f-160">Az.OperationalInsights</span></span>
- <span data-ttu-id="c685f-161">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-161">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="c685f-162">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c685f-162">Az.Profile</span></span>
- <span data-ttu-id="c685f-163">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="c685f-163">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c685f-164">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c685f-164">Az.RecoveryServices</span></span>
- <span data-ttu-id="c685f-165">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-165">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="c685f-166">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c685f-166">Az.Resources</span></span>
- <span data-ttu-id="c685f-167">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-167">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c685f-168">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c685f-168">Az.ServiceFabric</span></span>
- <span data-ttu-id="c685f-169">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="c685f-169">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="c685f-170">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-170">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="c685f-171">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="c685f-171">Az.SIgnalR</span></span>
- <span data-ttu-id="c685f-172">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="c685f-172">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="c685f-173">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c685f-173">Az.Sql</span></span>
- <span data-ttu-id="c685f-174">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="c685f-174">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="c685f-175">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="c685f-175">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="c685f-176">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-176">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="c685f-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c685f-177">Az.Storage</span></span>
- <span data-ttu-id="c685f-178">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-178">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c685f-179">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c685f-179">Az.Websites</span></span>
- <span data-ttu-id="c685f-180">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="c685f-180">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="c685f-181">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="c685f-181">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="c685f-182">一般</span><span class="sxs-lookup"><span data-stu-id="c685f-182">General</span></span>

* <span data-ttu-id="c685f-183">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="c685f-183">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="c685f-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c685f-184">Az.Compute</span></span>

* <span data-ttu-id="c685f-185">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="c685f-185">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="c685f-186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c685f-186">Az.DataLakeStore</span></span>

* <span data-ttu-id="c685f-187">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="c685f-187">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="c685f-188">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="c685f-188">Az.FrontDoor</span></span>

* <span data-ttu-id="c685f-189">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="c685f-189">Fixed some broken links</span></span>
    - <span data-ttu-id="c685f-190">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="c685f-190">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="c685f-191">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="c685f-191">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="c685f-192">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c685f-192">Az.RecoveryServices</span></span>

* <span data-ttu-id="c685f-193">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="c685f-193">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="c685f-194">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="c685f-194">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="c685f-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c685f-195">Az.Resources</span></span>

* <span data-ttu-id="c685f-196">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="c685f-196">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="c685f-197">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="c685f-197">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="c685f-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c685f-198">Az.Sql</span></span>

* <span data-ttu-id="c685f-199">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="c685f-199">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="c685f-200">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="c685f-200">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="c685f-201">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="c685f-201">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="c685f-202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="c685f-202">Az.Storage</span></span>

* <span data-ttu-id="c685f-203">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="c685f-203">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="c685f-204">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="c685f-204">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="c685f-205">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c685f-205">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c685f-206">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="c685f-206">Support Static Website configuration</span></span>
    - <span data-ttu-id="c685f-207">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c685f-207">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="c685f-208">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="c685f-208">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="c685f-209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c685f-209">Az.Websites</span></span>

* <span data-ttu-id="c685f-210">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c685f-210">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="c685f-211">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="c685f-211">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="c685f-212">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="c685f-212">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="c685f-213">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="c685f-213">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="c685f-214">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c685f-214">Az.ApiManagement</span></span>
* <span data-ttu-id="c685f-215">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="c685f-215">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="c685f-216">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="c685f-216">Az.Automation</span></span>
* <span data-ttu-id="c685f-217">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-217">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c685f-218">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-218">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c685f-219">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-219">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c685f-220">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-220">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c685f-221">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="c685f-221">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="c685f-222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c685f-222">Az.Compute</span></span>
* <span data-ttu-id="c685f-223">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="c685f-223">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c685f-224">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="c685f-224">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="c685f-225">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c685f-225">Az.ContainerInstance</span></span>
* <span data-ttu-id="c685f-226">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="c685f-226">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="c685f-227">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c685f-227">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="c685f-228">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="c685f-228">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="c685f-229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c685f-229">Az.Network</span></span>
* <span data-ttu-id="c685f-230">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="c685f-230">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c685f-231">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="c685f-231">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c685f-232">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="c685f-232">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="c685f-233">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="c685f-233">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="c685f-234">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c685f-234">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c685f-235">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="c685f-235">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c685f-236">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="c685f-236">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="c685f-237">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c685f-237">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c685f-238">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="c685f-238">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c685f-239">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="c685f-239">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="c685f-240">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="c685f-240">Az.Relay</span></span>
* <span data-ttu-id="c685f-241">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="c685f-241">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="c685f-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c685f-242">Az.Resources</span></span>
* <span data-ttu-id="c685f-243">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="c685f-243">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c685f-244">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="c685f-244">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c685f-245">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="c685f-245">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="c685f-246">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c685f-246">Az.ServiceFabric</span></span>
* <span data-ttu-id="c685f-247">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="c685f-247">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="c685f-248">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c685f-248">Az.Sql</span></span>
* <span data-ttu-id="c685f-249">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-249">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c685f-250">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c685f-250">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c685f-251">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c685f-251">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c685f-252">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c685f-252">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c685f-253">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c685f-253">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c685f-254">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c685f-254">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c685f-255">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c685f-255">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c685f-256">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c685f-256">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c685f-257">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c685f-257">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c685f-258">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="c685f-258">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c685f-259">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="c685f-259">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c685f-260">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="c685f-260">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c685f-261">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="c685f-261">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c685f-262">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="c685f-262">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c685f-263">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="c685f-263">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c685f-264">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="c685f-264">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c685f-265">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="c685f-265">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="c685f-266">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="c685f-266">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c685f-267">一般</span><span class="sxs-lookup"><span data-stu-id="c685f-267">General</span></span>
* <span data-ttu-id="c685f-268">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="c685f-268">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="c685f-269">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c685f-269">Az.Profile</span></span>
* <span data-ttu-id="c685f-270">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c685f-270">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c685f-271">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="c685f-271">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c685f-272">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="c685f-272">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="c685f-273">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="c685f-273">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c685f-274">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="c685f-274">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c685f-275">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="c685f-275">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c685f-276">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="c685f-276">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="c685f-277">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c685f-277">Az.CognitiveServices</span></span>
* <span data-ttu-id="c685f-278">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="c685f-278">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c685f-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c685f-279">Az.Compute</span></span>
* <span data-ttu-id="c685f-280">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-280">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c685f-281">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="c685f-281">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c685f-282">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="c685f-282">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c685f-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c685f-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="c685f-284">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="c685f-284">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c685f-285">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="c685f-285">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="c685f-286">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="c685f-286">Az.Insights</span></span>
* <span data-ttu-id="c685f-287">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="c685f-287">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c685f-288">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="c685f-288">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c685f-289">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="c685f-289">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c685f-290">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="c685f-290">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c685f-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c685f-291">Az.Network</span></span>
* <span data-ttu-id="c685f-292">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="c685f-292">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c685f-293">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c685f-293">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c685f-294">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c685f-294">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c685f-295">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c685f-295">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c685f-296">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c685f-296">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c685f-297">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c685f-297">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c685f-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c685f-298">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="c685f-299">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c685f-299">Az.PolicyInsights</span></span>
* <span data-ttu-id="c685f-300">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-300">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="c685f-301">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c685f-301">Az.Resources</span></span>
* <span data-ttu-id="c685f-302">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="c685f-302">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c685f-303">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="c685f-303">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="c685f-304">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c685f-304">Az.ServiceBus</span></span>
* <span data-ttu-id="c685f-305">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="c685f-305">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="c685f-306">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c685f-306">Az.ServiceFabric</span></span>
* <span data-ttu-id="c685f-307">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="c685f-307">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c685f-308">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="c685f-308">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c685f-309">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="c685f-309">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c685f-310">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="c685f-310">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c685f-311">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="c685f-311">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="c685f-312">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="c685f-312">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="c685f-313">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="c685f-313">Az.Profile</span></span>
* <span data-ttu-id="c685f-314">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="c685f-314">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="c685f-315">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c685f-315">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c685f-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c685f-316">Az.Compute</span></span>
* <span data-ttu-id="c685f-317">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="c685f-317">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="c685f-318">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c685f-318">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="c685f-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c685f-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="c685f-320">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="c685f-320">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c685f-321">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c685f-321">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c685f-322">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="c685f-322">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c685f-323">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c685f-323">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c685f-324">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c685f-324">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c685f-325">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c685f-325">Az.Network</span></span>
* <span data-ttu-id="c685f-326">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="c685f-326">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c685f-327">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c685f-327">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="c685f-328">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c685f-328">Az.Resources</span></span>
* <span data-ttu-id="c685f-329">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="c685f-329">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c685f-330">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="c685f-330">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="c685f-331">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="c685f-331">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c685f-332">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c685f-332">Azure.Storage</span></span>
* <span data-ttu-id="c685f-333">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="c685f-333">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c685f-334">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c685f-334">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c685f-335">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c685f-335">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="c685f-336">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="c685f-336">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c685f-337">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c685f-337">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="c685f-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c685f-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="c685f-339">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="c685f-339">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="c685f-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="c685f-340">Az.Compute</span></span>
* <span data-ttu-id="c685f-341">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="c685f-341">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c685f-342">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="c685f-342">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="c685f-343">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="c685f-343">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="c685f-344">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c685f-344">Az.DataFactoryV2</span></span>
* <span data-ttu-id="c685f-345">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="c685f-345">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="c685f-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="c685f-346">Az.Network</span></span>
* <span data-ttu-id="c685f-347">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="c685f-347">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c685f-348">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-348">new cmdlets added</span></span>
    - <span data-ttu-id="c685f-349">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c685f-349">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="c685f-350">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c685f-350">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="c685f-351">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c685f-351">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="c685f-352">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c685f-352">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="c685f-353">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c685f-353">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="c685f-354">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c685f-354">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c685f-355">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="c685f-355">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c685f-356">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-356">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="c685f-357">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c685f-357">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="c685f-358">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c685f-358">Az.RedisCache</span></span>
* <span data-ttu-id="c685f-359">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="c685f-359">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c685f-360">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="c685f-360">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="c685f-361">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="c685f-361">Az.Resources</span></span>
* <span data-ttu-id="c685f-362">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c685f-362">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="c685f-363">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="c685f-363">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="c685f-364">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="c685f-364">Az.Sql</span></span>
* <span data-ttu-id="c685f-365">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="c685f-365">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="c685f-366">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="c685f-366">Az.Websites</span></span>
* <span data-ttu-id="c685f-367">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="c685f-367">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c685f-368">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="c685f-368">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="c685f-369">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="c685f-369">0.2.0 - September 2018</span></span>
 <span data-ttu-id="c685f-370">初始版本</span><span class="sxs-lookup"><span data-stu-id="c685f-370">Initial Release</span></span>