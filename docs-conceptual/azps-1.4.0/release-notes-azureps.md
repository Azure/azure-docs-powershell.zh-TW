## <a name="140---february-2019"></a><span data-ttu-id="82842-101">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="82842-101">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="82842-102">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82842-102">Az.AnalysisServices</span></span>
* <span data-ttu-id="82842-103">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-103">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82842-104">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82842-104">Az.Automation</span></span>
* <span data-ttu-id="82842-105">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="82842-105">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="82842-106">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-106">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="82842-107">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="82842-107">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82842-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82842-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="82842-109">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="82842-109">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82842-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-110">Az.Compute</span></span>
* <span data-ttu-id="82842-111">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="82842-111">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="82842-112">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="82842-112">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="82842-113">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-113">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="82842-114">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="82842-114">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82842-115">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82842-115">Az.DataLakeStore</span></span>
* <span data-ttu-id="82842-116">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-116">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82842-117">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82842-117">Az.EventHub</span></span>
* <span data-ttu-id="82842-118">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="82842-118">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="82842-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82842-119">Az.KeyVault</span></span>
* <span data-ttu-id="82842-120">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="82842-120">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82842-121">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82842-121">Az.LogicApp</span></span>
* <span data-ttu-id="82842-122">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="82842-122">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="82842-123">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="82842-123">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="82842-124">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-124">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="82842-125">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="82842-125">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82842-126">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="82842-126">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82842-127">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="82842-127">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82842-128">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="82842-128">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="82842-129">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-129">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="82842-130">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="82842-130">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82842-131">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="82842-131">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82842-132">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="82842-132">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82842-133">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="82842-133">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="82842-134">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="82842-134">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82842-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82842-135">Az.Monitor</span></span>
* <span data-ttu-id="82842-136">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="82842-136">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82842-137">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82842-137">Az.Network</span></span>
* <span data-ttu-id="82842-138">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="82842-138">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82842-139">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82842-139">Az.OperationalInsights</span></span>
* <span data-ttu-id="82842-140">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="82842-140">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="82842-141">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="82842-141">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="82842-142">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="82842-142">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="82842-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-143">Az.Resources</span></span>
* <span data-ttu-id="82842-144">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="82842-144">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="82842-145">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="82842-145">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="82842-146">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="82842-146">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="82842-147">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="82842-147">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="82842-148">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82842-148">Az.Sql</span></span>
* <span data-ttu-id="82842-149">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="82842-149">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="82842-150">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="82842-150">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82842-151">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82842-151">Az.Websites</span></span>
* <span data-ttu-id="82842-152">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="82842-152">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="82842-153">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="82842-153">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82842-154">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82842-154">Az.Accounts</span></span>
* <span data-ttu-id="82842-155">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="82842-155">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82842-156">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82842-156">Az.AnalysisServices</span></span>
<span data-ttu-id="82842-157">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="82842-157">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82842-158">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-158">Az.Compute</span></span>
* <span data-ttu-id="82842-159">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="82842-159">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="82842-160">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="82842-160">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="82842-161">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="82842-161">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82842-162">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82842-162">Az.RecoveryServices</span></span>
<span data-ttu-id="82842-163">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="82842-163">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82842-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-164">Az.Resources</span></span>
* <span data-ttu-id="82842-165">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="82842-165">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="82842-166">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="82842-166">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="82842-167">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="82842-167">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="82842-168">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="82842-168">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="82842-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82842-169">Az.Sql</span></span>
* <span data-ttu-id="82842-170">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="82842-170">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="82842-171">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="82842-171">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="82842-172">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="82842-172">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="82842-173">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="82842-173">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82842-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82842-174">Az.Accounts</span></span>
* <span data-ttu-id="82842-175">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="82842-175">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82842-176">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82842-176">Az.AnalysisServices</span></span>
* <span data-ttu-id="82842-177">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="82842-177">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82842-178">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82842-178">Az.RecoveryServices</span></span>
* <span data-ttu-id="82842-179">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="82842-179">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="82842-180">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="82842-180">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82842-181">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82842-181">Az.Accounts</span></span>
* <span data-ttu-id="82842-182">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="82842-182">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="82842-183">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-183">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82842-184">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="82842-184">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="82842-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="82842-185">Az.Aks</span></span>
* <span data-ttu-id="82842-186">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-186">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82842-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82842-187">Az.Automation</span></span>
* <span data-ttu-id="82842-188">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="82842-188">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="82842-189">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-189">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82842-190">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82842-190">Az.Cdn</span></span>
* <span data-ttu-id="82842-191">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-191">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82842-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-192">Az.Compute</span></span>
* <span data-ttu-id="82842-193">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-193">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="82842-194">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82842-194">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="82842-195">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="82842-195">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="82842-196">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82842-196">Az.ContainerRegistry</span></span>
* <span data-ttu-id="82842-197">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-197">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82842-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82842-198">Az.DataFactory</span></span>
* <span data-ttu-id="82842-199">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="82842-199">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82842-200">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82842-200">Az.DataLakeStore</span></span>
* <span data-ttu-id="82842-201">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="82842-201">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="82842-202">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="82842-202">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="82842-203">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-203">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82842-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82842-204">Az.IotHub</span></span>
* <span data-ttu-id="82842-205">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82842-205">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82842-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82842-206">Az.KeyVault</span></span>
* <span data-ttu-id="82842-207">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-207">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82842-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82842-208">Az.Network</span></span>
* <span data-ttu-id="82842-209">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-209">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="82842-210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-210">Az.Resources</span></span>
* <span data-ttu-id="82842-211">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="82842-211">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="82842-212">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="82842-212">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="82842-213">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="82842-213">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="82842-214">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="82842-214">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="82842-215">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="82842-215">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="82842-216">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="82842-216">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="82842-217">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="82842-217">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82842-218">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82842-218">Az.ServiceFabric</span></span>
* <span data-ttu-id="82842-219">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="82842-219">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="82842-220">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="82842-220">Fix some error messages.</span></span>
* <span data-ttu-id="82842-221">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="82842-221">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="82842-222">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="82842-222">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="82842-223">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="82842-223">Az.SignalR</span></span>
* <span data-ttu-id="82842-224">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-224">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="82842-225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82842-225">Az.Sql</span></span>
* <span data-ttu-id="82842-226">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82842-227">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="82842-227">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="82842-228">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="82842-228">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="82842-229">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="82842-229">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82842-230">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82842-230">Az.Storage</span></span>
* <span data-ttu-id="82842-231">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-231">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82842-232">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="82842-232">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="82842-233">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="82842-233">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="82842-234">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="82842-234">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="82842-235">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="82842-235">Az.TrafficManager</span></span>
* <span data-ttu-id="82842-236">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-236">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82842-237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82842-237">Az.Websites</span></span>
* <span data-ttu-id="82842-238">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82842-238">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82842-239">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="82842-239">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="82842-240">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="82842-240">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="82842-241">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="82842-241">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82842-242">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82842-242">Az.Accounts</span></span>
* <span data-ttu-id="82842-243">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="82842-243">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82842-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-244">Az.Compute</span></span>
* <span data-ttu-id="82842-245">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="82842-245">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="82842-246">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="82842-246">Updated the description of ID in help files</span></span>
* <span data-ttu-id="82842-247">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="82842-247">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82842-248">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82842-248">Az.DataLakeStore</span></span>
* <span data-ttu-id="82842-249">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="82842-249">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="82842-250">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="82842-250">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="82842-251">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="82842-251">Az.EventGrid</span></span>
* <span data-ttu-id="82842-252">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="82842-252">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="82842-253">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="82842-253">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="82842-254">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="82842-254">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="82842-255">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="82842-255">Event Time-To-Live,</span></span>
        - <span data-ttu-id="82842-256">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="82842-256">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="82842-257">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="82842-257">Dead letter endpoint.</span></span>
    - <span data-ttu-id="82842-258">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="82842-258">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="82842-259">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="82842-259">Event Time-To-Live,</span></span>
        - <span data-ttu-id="82842-260">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="82842-260">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="82842-261">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="82842-261">Dead letter endpoint.</span></span>
* <span data-ttu-id="82842-262">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="82842-262">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="82842-263">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="82842-263">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82842-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82842-264">Az.IotHub</span></span>
* <span data-ttu-id="82842-265">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="82842-265">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82842-266">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82842-266">Az.LogicApp</span></span>
* <span data-ttu-id="82842-267">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="82842-267">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="82842-268">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-268">Az.Resources</span></span>
* <span data-ttu-id="82842-269">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="82842-269">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="82842-270">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="82842-270">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="82842-271">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="82842-271">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="82842-272">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="82842-272">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="82842-273">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="82842-273">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="82842-274">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="82842-274">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="82842-275">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="82842-275">Az.SignalR</span></span>
* <span data-ttu-id="82842-276">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="82842-276">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="82842-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82842-277">Az.Sql</span></span>
* <span data-ttu-id="82842-278">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="82842-278">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82842-279">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82842-279">Az.Storage</span></span>
* <span data-ttu-id="82842-280">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="82842-280">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="82842-281">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="82842-281">New-AzStorageContext</span></span>
* <span data-ttu-id="82842-282">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="82842-282">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="82842-283">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="82842-283">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82842-284">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82842-284">Az.Websites</span></span>
* <span data-ttu-id="82842-285">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="82842-285">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="82842-286">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="82842-286">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="82842-287">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="82842-287">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="82842-288">一般</span><span class="sxs-lookup"><span data-stu-id="82842-288">General</span></span>

- <span data-ttu-id="82842-289">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="82842-289">General Availability of Az Module</span></span>
- <span data-ttu-id="82842-290">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="82842-290">Online help for each module</span></span>
- <span data-ttu-id="82842-291">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="82842-291">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="82842-292">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-292">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="82842-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82842-293">Az.Accounts</span></span>
- <span data-ttu-id="82842-294">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="82842-294">Changed from Az.Profile</span></span>
- <span data-ttu-id="82842-295">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="82842-295">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="82842-296">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82842-296">Az.ApiManagement</span></span>
- <span data-ttu-id="82842-297">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="82842-297">Fixes for #7002</span></span>
- <span data-ttu-id="82842-298">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-298">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="82842-299">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82842-299">Az.Batch</span></span>
- <span data-ttu-id="82842-300">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="82842-300">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="82842-301">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="82842-301">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="82842-302">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-302">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="82842-303">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="82842-303">Az.Billing</span></span>
- <span data-ttu-id="82842-304">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-304">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="82842-305">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="82842-305">Az.CognitivServices</span></span>
- <span data-ttu-id="82842-306">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="82842-306">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="82842-307">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="82842-307">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="82842-308">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="82842-308">Az.ContainerInstance</span></span>
- <span data-ttu-id="82842-309">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="82842-309">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="82842-310">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="82842-310">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="82842-311">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-311">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="82842-312">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82842-312">Az.DataLakeStore</span></span>
- <span data-ttu-id="82842-313">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-313">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="82842-314">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82842-314">Az.Monitor</span></span>
- <span data-ttu-id="82842-315">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-315">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="82842-316">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82842-316">Az.KeyVault</span></span>
- <span data-ttu-id="82842-317">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="82842-317">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="82842-318">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="82842-318">Az.MachineLearning</span></span>
- <span data-ttu-id="82842-319">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-319">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="82842-320">Az.Media</span><span class="sxs-lookup"><span data-stu-id="82842-320">Az.Media</span></span>
- <span data-ttu-id="82842-321">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="82842-321">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="82842-322">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82842-322">Az.Network</span></span>
<span data-ttu-id="82842-323">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="82842-323">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="82842-324">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="82842-324">New cmdlets added:</span></span>
        - <span data-ttu-id="82842-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82842-325">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82842-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82842-326">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82842-327">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82842-327">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82842-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82842-328">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82842-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82842-329">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82842-330">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="82842-330">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="82842-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="82842-331">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="82842-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="82842-332">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="82842-333">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82842-333">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="82842-334">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82842-334">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="82842-335">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="82842-335">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="82842-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="82842-336">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="82842-337">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82842-337">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="82842-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="82842-338">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="82842-339">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="82842-339">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="82842-340">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-340">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="82842-341">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82842-341">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="82842-342">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82842-342">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="82842-343">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82842-343">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="82842-344">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-344">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="82842-345">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-345">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="82842-346">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82842-346">Az.OperationalInsights</span></span>
- <span data-ttu-id="82842-347">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-347">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="82842-348">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82842-348">Az.Profile</span></span>
- <span data-ttu-id="82842-349">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82842-349">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="82842-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82842-350">Az.RecoveryServices</span></span>
- <span data-ttu-id="82842-351">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-351">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="82842-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-352">Az.Resources</span></span>
- <span data-ttu-id="82842-353">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-353">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="82842-354">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82842-354">Az.ServiceFabric</span></span>
- <span data-ttu-id="82842-355">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="82842-355">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="82842-356">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-356">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="82842-357">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="82842-357">Az.SIgnalR</span></span>
- <span data-ttu-id="82842-358">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="82842-358">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="82842-359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82842-359">Az.Sql</span></span>
- <span data-ttu-id="82842-360">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="82842-360">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="82842-361">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="82842-361">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="82842-362">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-362">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="82842-363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82842-363">Az.Storage</span></span>
- <span data-ttu-id="82842-364">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-364">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="82842-365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82842-365">Az.Websites</span></span>
- <span data-ttu-id="82842-366">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82842-366">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="82842-367">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="82842-367">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="82842-368">一般</span><span class="sxs-lookup"><span data-stu-id="82842-368">General</span></span>

* <span data-ttu-id="82842-369">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="82842-369">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="82842-370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-370">Az.Compute</span></span>

* <span data-ttu-id="82842-371">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="82842-371">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="82842-372">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82842-372">Az.DataLakeStore</span></span>

* <span data-ttu-id="82842-373">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="82842-373">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="82842-374">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82842-374">Az.FrontDoor</span></span>

* <span data-ttu-id="82842-375">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="82842-375">Fixed some broken links</span></span>
    - <span data-ttu-id="82842-376">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="82842-376">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="82842-377">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="82842-377">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="82842-378">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82842-378">Az.RecoveryServices</span></span>

* <span data-ttu-id="82842-379">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="82842-379">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="82842-380">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="82842-380">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="82842-381">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-381">Az.Resources</span></span>

* <span data-ttu-id="82842-382">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="82842-382">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="82842-383">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="82842-383">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="82842-384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82842-384">Az.Sql</span></span>

* <span data-ttu-id="82842-385">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="82842-385">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="82842-386">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="82842-386">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="82842-387">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="82842-387">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="82842-388">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82842-388">Az.Storage</span></span>

* <span data-ttu-id="82842-389">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="82842-389">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="82842-390">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="82842-390">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="82842-391">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="82842-391">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="82842-392">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="82842-392">Support Static Website configuration</span></span>
    - <span data-ttu-id="82842-393">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="82842-393">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="82842-394">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="82842-394">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="82842-395">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82842-395">Az.Websites</span></span>

* <span data-ttu-id="82842-396">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="82842-396">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="82842-397">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="82842-397">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="82842-398">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="82842-398">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="82842-399">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="82842-399">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="82842-400">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82842-400">Az.ApiManagement</span></span>
* <span data-ttu-id="82842-401">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="82842-401">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="82842-402">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82842-402">Az.Automation</span></span>
* <span data-ttu-id="82842-403">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-403">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="82842-404">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-404">Added Update Management cmdlets</span></span>
* <span data-ttu-id="82842-405">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-405">Added Source Control cmdlets</span></span>
* <span data-ttu-id="82842-406">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-406">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="82842-407">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="82842-407">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="82842-408">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-408">Az.Compute</span></span>
* <span data-ttu-id="82842-409">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="82842-409">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="82842-410">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="82842-410">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="82842-411">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="82842-411">Az.ContainerInstance</span></span>
* <span data-ttu-id="82842-412">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="82842-412">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="82842-413">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="82842-413">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="82842-414">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="82842-414">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="82842-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82842-415">Az.Network</span></span>
* <span data-ttu-id="82842-416">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="82842-416">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="82842-417">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="82842-417">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="82842-418">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="82842-418">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="82842-419">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="82842-419">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="82842-420">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="82842-420">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="82842-421">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="82842-421">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="82842-422">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="82842-422">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="82842-423">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="82842-423">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="82842-424">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="82842-424">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="82842-425">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="82842-425">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="82842-426">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="82842-426">Az.Relay</span></span>
* <span data-ttu-id="82842-427">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="82842-427">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="82842-428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-428">Az.Resources</span></span>
* <span data-ttu-id="82842-429">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="82842-429">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="82842-430">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="82842-430">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="82842-431">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="82842-431">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="82842-432">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82842-432">Az.ServiceFabric</span></span>
* <span data-ttu-id="82842-433">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="82842-433">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="82842-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82842-434">Az.Sql</span></span>
* <span data-ttu-id="82842-435">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-435">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="82842-436">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="82842-436">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82842-437">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="82842-437">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82842-438">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="82842-438">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82842-439">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="82842-439">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82842-440">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82842-440">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82842-441">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82842-441">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82842-442">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82842-442">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82842-443">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82842-443">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="82842-444">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="82842-444">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="82842-445">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="82842-445">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="82842-446">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="82842-446">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="82842-447">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="82842-447">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="82842-448">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="82842-448">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="82842-449">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="82842-449">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="82842-450">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="82842-450">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="82842-451">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="82842-451">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="82842-452">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="82842-452">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="82842-453">一般</span><span class="sxs-lookup"><span data-stu-id="82842-453">General</span></span>
* <span data-ttu-id="82842-454">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="82842-454">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="82842-455">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82842-455">Az.Profile</span></span>
* <span data-ttu-id="82842-456">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="82842-456">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="82842-457">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="82842-457">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="82842-458">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="82842-458">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="82842-459">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="82842-459">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="82842-460">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="82842-460">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="82842-461">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="82842-461">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="82842-462">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="82842-462">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="82842-463">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82842-463">Az.CognitiveServices</span></span>
* <span data-ttu-id="82842-464">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="82842-464">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82842-465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-465">Az.Compute</span></span>
* <span data-ttu-id="82842-466">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-466">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="82842-467">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="82842-467">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="82842-468">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="82842-468">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82842-469">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82842-469">Az.DataLakeStore</span></span>
* <span data-ttu-id="82842-470">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="82842-470">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="82842-471">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="82842-471">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="82842-472">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="82842-472">Az.Insights</span></span>
* <span data-ttu-id="82842-473">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="82842-473">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="82842-474">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="82842-474">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="82842-475">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="82842-475">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="82842-476">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="82842-476">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82842-477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82842-477">Az.Network</span></span>
* <span data-ttu-id="82842-478">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="82842-478">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="82842-479">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="82842-479">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="82842-480">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="82842-480">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="82842-481">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="82842-481">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="82842-482">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="82842-482">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="82842-483">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="82842-483">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="82842-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="82842-484">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82842-485">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82842-485">Az.PolicyInsights</span></span>
* <span data-ttu-id="82842-486">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-486">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="82842-487">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-487">Az.Resources</span></span>
* <span data-ttu-id="82842-488">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="82842-488">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="82842-489">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="82842-489">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="82842-490">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82842-490">Az.ServiceBus</span></span>
* <span data-ttu-id="82842-491">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="82842-491">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82842-492">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82842-492">Az.ServiceFabric</span></span>
* <span data-ttu-id="82842-493">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="82842-493">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="82842-494">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="82842-494">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="82842-495">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="82842-495">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="82842-496">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="82842-496">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="82842-497">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="82842-497">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="82842-498">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="82842-498">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="82842-499">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82842-499">Az.Profile</span></span>
* <span data-ttu-id="82842-500">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="82842-500">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="82842-501">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="82842-501">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82842-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-502">Az.Compute</span></span>
* <span data-ttu-id="82842-503">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="82842-503">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="82842-504">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82842-504">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82842-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82842-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="82842-506">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="82842-506">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="82842-507">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="82842-507">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="82842-508">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="82842-508">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="82842-509">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="82842-509">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="82842-510">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="82842-510">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82842-511">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82842-511">Az.Network</span></span>
* <span data-ttu-id="82842-512">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="82842-512">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="82842-513">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82842-513">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82842-514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-514">Az.Resources</span></span>
* <span data-ttu-id="82842-515">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="82842-515">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="82842-516">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="82842-516">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="82842-517">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="82842-517">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="82842-518">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="82842-518">Azure.Storage</span></span>
* <span data-ttu-id="82842-519">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="82842-519">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="82842-520">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="82842-520">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="82842-521">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="82842-521">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="82842-522">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="82842-522">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="82842-523">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="82842-523">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="82842-524">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82842-524">Az.CognitiveServices</span></span>
* <span data-ttu-id="82842-525">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="82842-525">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82842-526">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82842-526">Az.Compute</span></span>
* <span data-ttu-id="82842-527">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="82842-527">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="82842-528">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="82842-528">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="82842-529">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="82842-529">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="82842-530">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="82842-530">Az.DataFactoryV2</span></span>
* <span data-ttu-id="82842-531">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="82842-531">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82842-532">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82842-532">Az.Network</span></span>
* <span data-ttu-id="82842-533">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="82842-533">Added NetworkProfile functionality.</span></span> <span data-ttu-id="82842-534">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-534">new cmdlets added</span></span>
    - <span data-ttu-id="82842-535">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82842-535">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="82842-536">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82842-536">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="82842-537">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82842-537">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="82842-538">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82842-538">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="82842-539">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="82842-539">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="82842-540">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="82842-540">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="82842-541">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="82842-541">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="82842-542">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-542">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="82842-543">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82842-543">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="82842-544">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="82842-544">Az.RedisCache</span></span>
* <span data-ttu-id="82842-545">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="82842-545">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="82842-546">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="82842-546">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="82842-547">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82842-547">Az.Resources</span></span>
* <span data-ttu-id="82842-548">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82842-548">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="82842-549">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="82842-549">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="82842-550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82842-550">Az.Sql</span></span>
* <span data-ttu-id="82842-551">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="82842-551">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82842-552">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82842-552">Az.Websites</span></span>
* <span data-ttu-id="82842-553">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="82842-553">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="82842-554">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="82842-554">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="82842-555">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="82842-555">0.2.0 - September 2018</span></span>
 <span data-ttu-id="82842-556">初始版本</span><span class="sxs-lookup"><span data-stu-id="82842-556">Initial Release</span></span>