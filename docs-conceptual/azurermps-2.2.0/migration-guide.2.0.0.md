# <a name="table-of-contents"></a><span data-ttu-id="253ca-101">目錄</span><span class="sxs-lookup"><span data-stu-id="253ca-101">Table of Contents</span></span>
1. [<span data-ttu-id="253ca-102">移除 Force 參數</span><span class="sxs-lookup"><span data-stu-id="253ca-102">Removal of Force parameters</span></span>](#removal-of-force-parameters)
2. [<span data-ttu-id="253ca-103">變更 Tag 參數</span><span class="sxs-lookup"><span data-stu-id="253ca-103">Change of Tag parameters</span></span>](#change-of-tag-parameters)
3. [<span data-ttu-id="253ca-104">Storage Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="253ca-104">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
4. [<span data-ttu-id="253ca-105">AD Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="253ca-105">Breaking changes to AD cmdlets</span></span>](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a><span data-ttu-id="253ca-106">移除 Force 參數</span><span class="sxs-lookup"><span data-stu-id="253ca-106">Removal of Force parameters</span></span>

<span data-ttu-id="253ca-107">在此版本中，我們已將所有已淘汰的 `Force` 參數從 Cmdlet 和相對應的警告中移除，該參數將不會出現在未來版本中。</span><span class="sxs-lookup"><span data-stu-id="253ca-107">This release, we removed all Obsolete `Force` parameters from cmdlets and the corresponding warnings that the parameter would be removed in a future release.</span></span>

<span data-ttu-id="253ca-108">此變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="253ca-108">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="253ca-109">**ApiManagement**</span><span class="sxs-lookup"><span data-stu-id="253ca-109">**ApiManagement**</span></span>
- <span data-ttu-id="253ca-110">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="253ca-110">Remove-AzureRmApiManagement</span></span>
- <span data-ttu-id="253ca-111">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="253ca-111">Remove-AzureRmApiManagementApi</span></span>
- <span data-ttu-id="253ca-112">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="253ca-112">Remove-AzureRmApiManagementGroup</span></span>
- <span data-ttu-id="253ca-113">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="253ca-113">Remove-AzureRmApiManagementLogger</span></span>
- <span data-ttu-id="253ca-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="253ca-114">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>
- <span data-ttu-id="253ca-115">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="253ca-115">Remove-AzureRmApiManagementOperation</span></span>
- <span data-ttu-id="253ca-116">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="253ca-116">Remove-AzureRmApiManagementPolicy</span></span>
- <span data-ttu-id="253ca-117">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="253ca-117">Remove-AzureRmApiManagementProduct</span></span>
- <span data-ttu-id="253ca-118">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="253ca-118">Remove-AzureRmApiManagementProperty</span></span>
- <span data-ttu-id="253ca-119">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="253ca-119">Remove-AzureRmApiManagementSubscription</span></span>
- <span data-ttu-id="253ca-120">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="253ca-120">Remove-AzureRmApiManagementUser</span></span>

<span data-ttu-id="253ca-121">**自動化**</span><span class="sxs-lookup"><span data-stu-id="253ca-121">**Automation**</span></span>
- <span data-ttu-id="253ca-122">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="253ca-122">Remove-AzureRmAutomationCertificate</span></span>
- <span data-ttu-id="253ca-123">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="253ca-123">Remove-AzureRmAutomationCredential</span></span>
- <span data-ttu-id="253ca-124">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="253ca-124">Remove-AzureRmAutomationVariable</span></span>
- <span data-ttu-id="253ca-125">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="253ca-125">Remove-AzureRmAutomationWebhook</span></span>

<span data-ttu-id="253ca-126">**Batch**</span><span class="sxs-lookup"><span data-stu-id="253ca-126">**Batch**</span></span>
- <span data-ttu-id="253ca-127">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="253ca-127">Remove-AzureBatchCertificate</span></span>
- <span data-ttu-id="253ca-128">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="253ca-128">Remove-AzureBatchComputeNode</span></span>
- <span data-ttu-id="253ca-129">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="253ca-129">Remove-AzureBatchComputeNodeUser</span></span>

<span data-ttu-id="253ca-130">**DataFactories**</span><span class="sxs-lookup"><span data-stu-id="253ca-130">**DataFactories**</span></span>
- <span data-ttu-id="253ca-131">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="253ca-131">Resume-AzureRmDataFactoryPipeline</span></span>
- <span data-ttu-id="253ca-132">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="253ca-132">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>
- <span data-ttu-id="253ca-133">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="253ca-133">Suspend-AzureRmDataFactoryPipeline</span></span>

<span data-ttu-id="253ca-134">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="253ca-134">**DataLakeStore**</span></span>
- <span data-ttu-id="253ca-135">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="253ca-135">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="253ca-136">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="253ca-136">Set-AzureRmDataLakeStoreItemAcl</span></span>
- <span data-ttu-id="253ca-137">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="253ca-137">Set-AzureRmDataLakeStoreItemAclEntry</span></span>
- <span data-ttu-id="253ca-138">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="253ca-138">Set-AzureRmDataLakeStoreItemOwner</span></span>

<span data-ttu-id="253ca-139">**OperationalInsights**</span><span class="sxs-lookup"><span data-stu-id="253ca-139">**OperationalInsights**</span></span>
- <span data-ttu-id="253ca-140">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="253ca-140">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

<span data-ttu-id="253ca-141">**設定檔**</span><span class="sxs-lookup"><span data-stu-id="253ca-141">**Profile**</span></span>
- <span data-ttu-id="253ca-142">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="253ca-142">Remove-AzureRmEnvironment</span></span>

<span data-ttu-id="253ca-143">**RedisCache**</span><span class="sxs-lookup"><span data-stu-id="253ca-143">**RedisCache**</span></span>
- <span data-ttu-id="253ca-144">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="253ca-144">Remove-AzureRmRedisCacheDiagnostics</span></span>

<span data-ttu-id="253ca-145">**資源**</span><span class="sxs-lookup"><span data-stu-id="253ca-145">**Resources**</span></span>
- <span data-ttu-id="253ca-146">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="253ca-146">Register-AzureRmProviderFeature</span></span>
- <span data-ttu-id="253ca-147">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="253ca-147">Register-AzureRmResourceProvider</span></span>
- <span data-ttu-id="253ca-148">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="253ca-148">Remove-AzureRmADServicePrincipal</span></span>
- <span data-ttu-id="253ca-149">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="253ca-149">Remove-AzureRmPolicyAssignment</span></span>
- <span data-ttu-id="253ca-150">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="253ca-150">Remove-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="253ca-151">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="253ca-151">Remove-AzureRmRoleAssignment</span></span>
- <span data-ttu-id="253ca-152">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="253ca-152">Stop-AzureRmResourceGroupDeployment</span></span>
- <span data-ttu-id="253ca-153">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="253ca-153">Unregister-AzureRmResourceProvider</span></span>

<span data-ttu-id="253ca-154">**儲存體**</span><span class="sxs-lookup"><span data-stu-id="253ca-154">**Storage**</span></span>
- <span data-ttu-id="253ca-155">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="253ca-155">Remove-AzureStorageContainerStoredAccessPolicy</span></span>
- <span data-ttu-id="253ca-156">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="253ca-156">Remove-AzureStorageQueueStoredAccessPolicy</span></span>
- <span data-ttu-id="253ca-157">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="253ca-157">Remove-AzureStorageShareStoredAccessPolicy</span></span>
- <span data-ttu-id="253ca-158">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="253ca-158">Remove-AzureStorageTableStoredAccessPolicy</span></span>

<span data-ttu-id="253ca-159">**StreamAnalytics**</span><span class="sxs-lookup"><span data-stu-id="253ca-159">**StreamAnalytics**</span></span>
- <span data-ttu-id="253ca-160">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="253ca-160">Remove-AzureRmStreamAnalyticsFunction</span></span>
- <span data-ttu-id="253ca-161">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="253ca-161">Remove-AzureRmStreamAnalyticsInput</span></span>
- <span data-ttu-id="253ca-162">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="253ca-162">Remove-AzureRmStreamAnalyticsJob</span></span>
- <span data-ttu-id="253ca-163">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="253ca-163">Remove-AzureRmStreamAnalyticsOutput</span></span>

<span data-ttu-id="253ca-164">**Tag**</span><span class="sxs-lookup"><span data-stu-id="253ca-164">**Tag**</span></span>
- <span data-ttu-id="253ca-165">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="253ca-165">Remove-AzureRmTag</span></span>

<br>

<span data-ttu-id="253ca-166">如果您有使用上述任何 Cmdlet 的指令碼，只要移除 `Force` 參數，即可修正此重大變更。</span><span class="sxs-lookup"><span data-stu-id="253ca-166">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by simply removing the `Force` parameter.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a><span data-ttu-id="253ca-167">變更 Tag 參數</span><span class="sxs-lookup"><span data-stu-id="253ca-167">Change of Tag parameters</span></span>

<span data-ttu-id="253ca-168">在此版本中，`Tags` 參數名稱已變更為 `Tag`，而類型已從 `Hashtable[]` 變更為 `Hashtable`，變更了機碼值組的格式。</span><span class="sxs-lookup"><span data-stu-id="253ca-168">This release, the `Tags` parameter name was changed to `Tag`, and the type was changed from `Hashtable[]` to `Hashtable`, changing the format of the key-value pairings.</span></span>

<span data-ttu-id="253ca-169">先前，`Hashtable[]` 中的每個項目代表單一機碼值組：</span><span class="sxs-lookup"><span data-stu-id="253ca-169">Previously, each entry in the `Hashtable[]` represented a single key-value pairing:</span></span>

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

<span data-ttu-id="253ca-170">現在則不再需要 `Name` 和 `Value`，只要在 `Hashtable` 中指派 `Key = "Value"` 即可建立機碼值組：</span><span class="sxs-lookup"><span data-stu-id="253ca-170">Now, `Name` and `Value` are no longer necessary, allowing for key-value pairings to be created by assigning `Key = "Value"` in the `Hashtable`:</span></span>

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

<span data-ttu-id="253ca-171">此變更會影響下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="253ca-171">The following cmdlets are affected by this change:</span></span>

<span data-ttu-id="253ca-172">**Batch**</span><span class="sxs-lookup"><span data-stu-id="253ca-172">**Batch**</span></span>
- <span data-ttu-id="253ca-173">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-173">Get-AzureRmBatchAccount</span></span>
- <span data-ttu-id="253ca-174">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-174">New-AzureRmBatchAccount</span></span>
- <span data-ttu-id="253ca-175">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-175">Set-AzureRmBatchAccount</span></span>

<span data-ttu-id="253ca-176">**計算**</span><span class="sxs-lookup"><span data-stu-id="253ca-176">**Compute**</span></span>
- <span data-ttu-id="253ca-177">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="253ca-177">New-AzureRmVM</span></span>
- <span data-ttu-id="253ca-178">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="253ca-178">Update-AzureRmVM</span></span>

<span data-ttu-id="253ca-179">**DataLakeAnalytics**</span><span class="sxs-lookup"><span data-stu-id="253ca-179">**DataLakeAnalytics**</span></span>
- <span data-ttu-id="253ca-180">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-180">New-AzureRmDataLakeAnalyticsAccount</span></span>
- <span data-ttu-id="253ca-181">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-181">Set-AzureRmDataLakeAnalyticsAccount</span></span>

<span data-ttu-id="253ca-182">**DataLakeStore**</span><span class="sxs-lookup"><span data-stu-id="253ca-182">**DataLakeStore**</span></span>
- <span data-ttu-id="253ca-183">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-183">New-AzureRmDataLakeStoreAccount</span></span>
- <span data-ttu-id="253ca-184">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-184">Set-AzureRmDataLakeStoreAccount</span></span>

<span data-ttu-id="253ca-185">**Dns**</span><span class="sxs-lookup"><span data-stu-id="253ca-185">**Dns**</span></span>
- <span data-ttu-id="253ca-186">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="253ca-186">New-AzureRmDnsZone</span></span>
- <span data-ttu-id="253ca-187">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="253ca-187">Set-AzureRmDnsZone</span></span>

<span data-ttu-id="253ca-188">**KeyVault**</span><span class="sxs-lookup"><span data-stu-id="253ca-188">**KeyVault**</span></span>
- <span data-ttu-id="253ca-189">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="253ca-189">Get-AzureRmKeyVault</span></span>
- <span data-ttu-id="253ca-190">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="253ca-190">New-AzureRmKeyVault</span></span>

<span data-ttu-id="253ca-191">**網路**</span><span class="sxs-lookup"><span data-stu-id="253ca-191">**Network**</span></span>
- <span data-ttu-id="253ca-192">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="253ca-192">New-AzureRmApplicationGateway</span></span>
- <span data-ttu-id="253ca-193">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="253ca-193">New-AzureRmExpressRouteCircuit</span></span>
- <span data-ttu-id="253ca-194">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="253ca-194">New-AzureRmLoadBalancer</span></span>
- <span data-ttu-id="253ca-195">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="253ca-195">New-AzureRmLocalNetworkGateway</span></span>
- <span data-ttu-id="253ca-196">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="253ca-196">New-AzureRmNetworkInterface</span></span>
- <span data-ttu-id="253ca-197">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="253ca-197">New-AzureRmNetworkSecurityGroup</span></span>
- <span data-ttu-id="253ca-198">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="253ca-198">New-AzureRmPublicIpAddress</span></span>
- <span data-ttu-id="253ca-199">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="253ca-199">New-AzureRmRouteTable</span></span>
- <span data-ttu-id="253ca-200">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="253ca-200">New-AzureRmVirtualNetwork</span></span>
- <span data-ttu-id="253ca-201">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="253ca-201">New-AzureRmVirtualNetworkGateway</span></span>
- <span data-ttu-id="253ca-202">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="253ca-202">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="253ca-203">New-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="253ca-203">New-AzureRmVirtualNetworkPeering</span></span>

<span data-ttu-id="253ca-204">**資源**</span><span class="sxs-lookup"><span data-stu-id="253ca-204">**Resources**</span></span>
- <span data-ttu-id="253ca-205">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="253ca-205">Find-AzureRmResource</span></span>
- <span data-ttu-id="253ca-206">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="253ca-206">Find-AzureRmResourceGroup</span></span>
- <span data-ttu-id="253ca-207">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="253ca-207">New-AzureRmResource</span></span>
- <span data-ttu-id="253ca-208">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="253ca-208">New-AzureRmResourceGroup</span></span>
- <span data-ttu-id="253ca-209">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="253ca-209">Set-AzureRmResource</span></span>
- <span data-ttu-id="253ca-210">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="253ca-210">Set-AzureRmResourceGroup</span></span>

<span data-ttu-id="253ca-211">**SQL**</span><span class="sxs-lookup"><span data-stu-id="253ca-211">**SQL**</span></span>
- <span data-ttu-id="253ca-212">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="253ca-212">New-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="253ca-213">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="253ca-213">New-AzureRmSqlDatabaseCopy</span></span>
- <span data-ttu-id="253ca-214">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="253ca-214">New-AzureRmSqlDatabaseSecondary</span></span>
- <span data-ttu-id="253ca-215">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="253ca-215">New-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="253ca-216">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="253ca-216">New-AzureRmSqlServer</span></span>
- <span data-ttu-id="253ca-217">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="253ca-217">Set-AzureRmSqlDatabase</span></span>
- <span data-ttu-id="253ca-218">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="253ca-218">Set-AzureRmSqlElasticPool</span></span>
- <span data-ttu-id="253ca-219">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="253ca-219">Set-AzureRmSqlServer</span></span>

<span data-ttu-id="253ca-220">**儲存體**</span><span class="sxs-lookup"><span data-stu-id="253ca-220">**Storage**</span></span>
- <span data-ttu-id="253ca-221">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-221">New-AzureRmStorageAccount</span></span>
- <span data-ttu-id="253ca-222">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="253ca-222">Set-AzureRmStorageAccount</span></span>

<span data-ttu-id="253ca-223">**TrafficManager**</span><span class="sxs-lookup"><span data-stu-id="253ca-223">**TrafficManager**</span></span>
- <span data-ttu-id="253ca-224">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="253ca-224">New-AzureRmTrafficManagerProfile</span></span>

<br>

<span data-ttu-id="253ca-225">如果您有使用上述任何 Cmdlet 的指令碼，只要將 `Tags` 參數變更為 `Tag`，以及將 `Tag` 變更為新格式，即可修正此重大變更</span><span class="sxs-lookup"><span data-stu-id="253ca-225">If you have a script that uses any of the above cmdlets, the breaking change can be fixed by changing the `Tags` parameter to `Tag`, as well as changing the `Tag` to the new format.</span></span>

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="253ca-226">Storage Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="253ca-226">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="253ca-227">受到此版本影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="253ca-227">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="253ca-228">**Get-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="253ca-228">**Get-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="253ca-229">Cmdlet 現在會傳回索引碼清單，而不是傳回具有每個索引碼屬性的物件</span><span class="sxs-lookup"><span data-stu-id="253ca-229">The cmdlet now returns a list of keys, rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

<span data-ttu-id="253ca-230">**New-AzureRmStorageAccountKey**</span><span class="sxs-lookup"><span data-stu-id="253ca-230">**New-AzureRmStorageAccountKey**</span></span>
- <span data-ttu-id="253ca-231">在此 Cmdlet 的輸出中，`StorageAccountRegenerateKeyResponse` 欄位已重新命名為 `StorageAccountListKeysResults`，這現在是索引碼清單，不是具有每個索引碼屬性的物件</span><span class="sxs-lookup"><span data-stu-id="253ca-231">`StorageAccountRegenerateKeyResponse` field in output of this cmdlet is renamed to `StorageAccountListKeysResults`, which is now a list of keys rather than an object with properties for each key</span></span>

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

<span data-ttu-id="253ca-232">**New/Get/Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="253ca-232">**New/Get/Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="253ca-233">在此 Cmdlet 的輸出中，`AccountType` 欄位已重新命名為 `Sku.Name`</span><span class="sxs-lookup"><span data-stu-id="253ca-233">`AccountType` field in output of this cmdlet is renamed to `Sku.Name`</span></span>
- <span data-ttu-id="253ca-234">將 PrimaryEndpoints/次要端點 blob/資料表/佇列/檔案的輸出類型從 `Uri` 變更為 `String`</span><span class="sxs-lookup"><span data-stu-id="253ca-234">Output type for PrimaryEndpoints/Secondary endpoints blob/table/queue/file changed from `Uri` to `String`</span></span>

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a><span data-ttu-id="253ca-235">AD Cmdlet 的重大變更</span><span class="sxs-lookup"><span data-stu-id="253ca-235">Breaking changes to AD cmdlets</span></span>

<span data-ttu-id="253ca-236">受到此版本影響的 Cmdlet 如下：</span><span class="sxs-lookup"><span data-stu-id="253ca-236">The following cmdlets were affected this release:</span></span>

<span data-ttu-id="253ca-237">**Get-AzureRMADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="253ca-237">**Get-AzureRMADServicePrincipal**</span></span>
- <span data-ttu-id="253ca-238">在此 Cmdlet 的輸出中，`ServicePrincipalName` 欄位已重新命名為 `ServicePrincipalNames`，且此欄位現在是集合。</span><span class="sxs-lookup"><span data-stu-id="253ca-238">`ServicePrincipalName` field in output of this cmdlet is renamed to `ServicePrincipalNames` and is now a collection.</span></span> <span data-ttu-id="253ca-239">其現在也會將 `ApplicationId` 顯示為其中一個 SPN (連同 identifierUri 一起)。</span><span class="sxs-lookup"><span data-stu-id="253ca-239">It now displays `ApplicationId` also as one of the SPN, along with the identifierUri.</span></span>

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

<span data-ttu-id="253ca-240">**Get-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="253ca-240">**Get-AzureRmADApplication**</span></span>
- <span data-ttu-id="253ca-241">`ApplicationObjectId` 參數已重新命名為 `ObjectId`。</span><span class="sxs-lookup"><span data-stu-id="253ca-241">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="253ca-242">在此 Cmdlet 的輸出中，`ApplicationObjectId` 已重新命名為 `ObjectId`</span><span class="sxs-lookup"><span data-stu-id="253ca-242">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

<span data-ttu-id="253ca-243">**Remove-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="253ca-243">**Remove-AzureRmADApplication**</span></span>
- <span data-ttu-id="253ca-244">`ApplicationObjectId` 參數已重新命名為 `ObjectId`。</span><span class="sxs-lookup"><span data-stu-id="253ca-244">Parameter `ApplicationObjectId` is renamed to `ObjectId`.</span></span>

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

<span data-ttu-id="253ca-245">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="253ca-245">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="253ca-246">在此 Cmdlet 的輸出中，`ApplicationObjectId` 已重新命名為 `ObjectId`</span><span class="sxs-lookup"><span data-stu-id="253ca-246">In output of this cmdlet, `ApplicationObjectId` is renamed to `ObjectId`.</span></span>
- <span data-ttu-id="253ca-247">已移除 `KeyValue`、`KeyUsage` 和 `KeyType` 參數</span><span class="sxs-lookup"><span data-stu-id="253ca-247">`KeyValue`, `KeyUsage`, `KeyType` parameters are removed.</span></span>

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

<span data-ttu-id="253ca-248">**Get-AzureRmADGroup**</span><span class="sxs-lookup"><span data-stu-id="253ca-248">**Get-AzureRmADGroup**</span></span>
- <span data-ttu-id="253ca-249">`Mail` 欄位已從輸出中移除。</span><span class="sxs-lookup"><span data-stu-id="253ca-249">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="253ca-250">**Get-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="253ca-250">**Get-AzureRmADUser**</span></span>
- <span data-ttu-id="253ca-251">`Mail` 欄位已從輸出中移除。</span><span class="sxs-lookup"><span data-stu-id="253ca-251">`Mail` field is removed from the output.</span></span>

<span data-ttu-id="253ca-252">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="253ca-252">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="253ca-253">已移除 `DisableAccount` 參數。</span><span class="sxs-lookup"><span data-stu-id="253ca-253">Removed `DisableAccount` parameter.</span></span>

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```