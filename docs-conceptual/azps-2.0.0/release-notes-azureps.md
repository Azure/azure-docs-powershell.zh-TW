---
ms.openlocfilehash: 3848f7fb8e298d137c747405f32a0776c1a8f029
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048626"
---
## <a name="200---may-2019"></a><span data-ttu-id="08d73-101">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="08d73-101">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d73-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-102">Az.Accounts</span></span>
* <span data-ttu-id="08d73-103">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="08d73-103">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d73-104">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d73-104">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d73-105">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="08d73-105">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="08d73-106">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="08d73-106">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-107">Az.Compute</span></span>
* <span data-ttu-id="08d73-108">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="08d73-108">Proximity placement group feature.</span></span>
    - <span data-ttu-id="08d73-109">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="08d73-109">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="08d73-110">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="08d73-110">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="08d73-111">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="08d73-111">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="08d73-112">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="08d73-112">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="08d73-113">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08d73-113">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="08d73-114">重大變更</span><span class="sxs-lookup"><span data-stu-id="08d73-114">Breaking changes</span></span>
    - <span data-ttu-id="08d73-115">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="08d73-115">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="08d73-116">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="08d73-116">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="08d73-117">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="08d73-117">Az.DeploymentManager</span></span>
* <span data-ttu-id="08d73-118">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-118">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="08d73-119">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="08d73-119">Az.Dns</span></span>
* <span data-ttu-id="08d73-120">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="08d73-120">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="08d73-121">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="08d73-121">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="08d73-122">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="08d73-122">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="08d73-123">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d73-123">Az.FrontDoor</span></span>
* <span data-ttu-id="08d73-124">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-124">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="08d73-125">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="08d73-125">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="08d73-126">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d73-126">Az.HDInsight</span></span>
* <span data-ttu-id="08d73-127">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="08d73-127">Removed two cmdlets:</span></span>
    - <span data-ttu-id="08d73-128">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08d73-128">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="08d73-129">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08d73-129">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="08d73-130">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="08d73-130">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="08d73-131">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="08d73-131">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="08d73-132">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="08d73-132">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="08d73-133">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="08d73-133">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d73-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d73-134">Az.Monitor</span></span>
* <span data-ttu-id="08d73-135">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="08d73-135">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="08d73-136">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="08d73-136">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="08d73-137">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="08d73-137">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="08d73-138">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="08d73-138">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="08d73-139">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="08d73-139">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="08d73-140">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="08d73-140">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="08d73-141">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="08d73-141">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="08d73-142">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d73-142">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d73-143">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d73-143">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d73-144">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d73-144">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d73-145">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d73-145">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d73-146">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="08d73-146">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="08d73-147">[更多](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="08d73-147">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="08d73-148">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-148">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-149">Az.Network</span></span>
* <span data-ttu-id="08d73-150">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-150">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="08d73-151">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-151">New cmdlets</span></span>
        - <span data-ttu-id="08d73-152">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08d73-152">New-AzNatGateway</span></span>
        - <span data-ttu-id="08d73-153">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08d73-153">Get-AzNatGateway</span></span>
        - <span data-ttu-id="08d73-154">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08d73-154">Set-AzNatGateway</span></span>
        - <span data-ttu-id="08d73-155">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="08d73-155">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="08d73-156">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-156">Updated cmdlets</span></span>
        - <span data-ttu-id="08d73-157">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="08d73-157">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="08d73-158">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="08d73-158">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="08d73-159">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="08d73-159">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="08d73-160">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="08d73-160">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="08d73-161">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="08d73-161">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d73-162">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d73-162">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d73-163">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="08d73-163">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="08d73-164">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="08d73-164">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="08d73-165">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="08d73-165">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d73-166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d73-166">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d73-167">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="08d73-167">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="08d73-168">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="08d73-168">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="08d73-169">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="08d73-169">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="08d73-170">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="08d73-170">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="08d73-171">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="08d73-171">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="08d73-172">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="08d73-172">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="08d73-173">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="08d73-173">Az.Relay</span></span>
* <span data-ttu-id="08d73-174">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="08d73-174">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08d73-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08d73-175">Az.ServiceBus</span></span>
* <span data-ttu-id="08d73-176">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-176">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d73-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-177">Az.Storage</span></span>
* <span data-ttu-id="08d73-178">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage.*' 變更為 'Microsoft.Azure.Storage.*')</span><span class="sxs-lookup"><span data-stu-id="08d73-178">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="08d73-179">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="08d73-179">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="08d73-180">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="08d73-180">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="08d73-181">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d73-181">New-AzStorageAccount</span></span>
* <span data-ttu-id="08d73-182">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="08d73-182">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="08d73-183">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d73-183">New-AzStorageAccount</span></span>
    - <span data-ttu-id="08d73-184">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d73-184">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="08d73-185">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d73-185">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d73-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-186">Az.Websites</span></span>
* <span data-ttu-id="08d73-187">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="08d73-187">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="08d73-188">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="08d73-188">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="08d73-189">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="08d73-189">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d73-190">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="08d73-190">Highlights since the last major release</span></span>
* <span data-ttu-id="08d73-191">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="08d73-191">General availability of `Az` module</span></span>
* <span data-ttu-id="08d73-192">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08d73-192">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08d73-193">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08d73-193">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08d73-194">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="08d73-194">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08d73-195">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="08d73-195">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08d73-196">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-196">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08d73-197">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-197">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d73-198">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-198">Az.Accounts</span></span>
* <span data-ttu-id="08d73-199">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="08d73-199">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="08d73-200">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08d73-200">Az.Batch</span></span>
* <span data-ttu-id="08d73-201">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-201">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d73-202">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d73-202">Az.Cdn</span></span>
* <span data-ttu-id="08d73-203">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d73-204">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d73-204">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d73-205">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-205">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-206">Az.Compute</span></span>
* <span data-ttu-id="08d73-207">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="08d73-207">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="08d73-208">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d73-209">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="08d73-209">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d73-210">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d73-210">Az.DataFactory</span></span>
* <span data-ttu-id="08d73-211">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="08d73-211">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d73-212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d73-212">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d73-213">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-213">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08d73-214">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08d73-214">Az.EventGrid</span></span>
* <span data-ttu-id="08d73-215">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08d73-215">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d73-216">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d73-216">Az.EventHub</span></span>
* <span data-ttu-id="08d73-217">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-217">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="08d73-218">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="08d73-218">Az.HDInsight</span></span>
* <span data-ttu-id="08d73-219">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d73-220">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d73-220">Az.IotHub</span></span>
* <span data-ttu-id="08d73-221">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d73-222">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d73-222">Az.KeyVault</span></span>
* <span data-ttu-id="08d73-223">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d73-224">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="08d73-224">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="08d73-225">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08d73-225">Az.MachineLearning</span></span>
* <span data-ttu-id="08d73-226">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-226">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="08d73-227">Az.Media</span><span class="sxs-lookup"><span data-stu-id="08d73-227">Az.Media</span></span>
* <span data-ttu-id="08d73-228">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-228">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d73-229">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d73-229">Az.Monitor</span></span>
  * <span data-ttu-id="08d73-230">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-230">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="08d73-231">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="08d73-231">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="08d73-232">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="08d73-232">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="08d73-233">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08d73-233">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="08d73-234">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08d73-234">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="08d73-235">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="08d73-235">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="08d73-236">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="08d73-236">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-237">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-237">Az.Network</span></span>
* <span data-ttu-id="08d73-238">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d73-239">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="08d73-239">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="08d73-240">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="08d73-240">Az.NotificationHubs</span></span>
* <span data-ttu-id="08d73-241">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-241">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08d73-242">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d73-242">Az.OperationalInsights</span></span>
* <span data-ttu-id="08d73-243">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="08d73-244">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="08d73-244">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="08d73-245">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d73-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d73-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d73-247">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d73-248">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="08d73-248">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="08d73-249">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="08d73-249">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="08d73-250">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="08d73-250">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08d73-251">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08d73-251">Az.RedisCache</span></span>
* <span data-ttu-id="08d73-252">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-253">Az.Resources</span></span>
* <span data-ttu-id="08d73-254">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="08d73-254">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-255">Az.Sql</span></span>
* <span data-ttu-id="08d73-256">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="08d73-256">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="08d73-257">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d73-258">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="08d73-258">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="08d73-259">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="08d73-259">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="08d73-260">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="08d73-260">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="08d73-261">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="08d73-261">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="08d73-262">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="08d73-262">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d73-263">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-263">Az.Websites</span></span>
* <span data-ttu-id="08d73-264">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="08d73-264">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="08d73-265">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="08d73-266">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="08d73-266">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="08d73-267">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="08d73-267">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="08d73-268">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="08d73-268">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d73-269">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="08d73-269">Highlights since the last major release</span></span>
* <span data-ttu-id="08d73-270">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="08d73-270">General availability of `Az` module</span></span>
* <span data-ttu-id="08d73-271">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08d73-271">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08d73-272">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08d73-272">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08d73-273">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="08d73-273">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08d73-274">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="08d73-274">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08d73-275">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-275">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08d73-276">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-276">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="08d73-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-277">Az.Accounts</span></span>
* <span data-ttu-id="08d73-278">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="08d73-278">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08d73-279">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08d73-279">Az.AnalysisServices</span></span>
* <span data-ttu-id="08d73-280">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="08d73-280">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="08d73-281">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="08d73-281">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d73-282">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d73-282">Az.Automation</span></span>
* <span data-ttu-id="08d73-283">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="08d73-283">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="08d73-284">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="08d73-284">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="08d73-285">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="08d73-285">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-286">Az.Compute</span></span>
* <span data-ttu-id="08d73-287">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="08d73-287">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="08d73-288">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="08d73-288">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="08d73-289">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08d73-289">Az.ContainerInstance</span></span>
* <span data-ttu-id="08d73-290">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="08d73-290">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d73-291">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d73-291">Az.DataFactory</span></span>
* <span data-ttu-id="08d73-292">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="08d73-292">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="08d73-293">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08d73-293">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-294">Az.Resources</span></span>
* <span data-ttu-id="08d73-295">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="08d73-295">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="08d73-296">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="08d73-296">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="08d73-297">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="08d73-297">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="08d73-298">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="08d73-298">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="08d73-299">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="08d73-299">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="08d73-300">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="08d73-300">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-301">Az.Sql</span></span>
* <span data-ttu-id="08d73-302">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="08d73-302">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d73-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-303">Az.Storage</span></span>
* <span data-ttu-id="08d73-304">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="08d73-304">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="08d73-305">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="08d73-305">New-AzStorageContext</span></span>
* <span data-ttu-id="08d73-306">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="08d73-306">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="08d73-307">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="08d73-307">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="08d73-308">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="08d73-308">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="08d73-309">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08d73-309">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="08d73-310">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08d73-310">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="08d73-311">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-311">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="08d73-312">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08d73-312">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="08d73-313">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="08d73-313">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="08d73-314">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08d73-314">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="08d73-315">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="08d73-315">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="08d73-316">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="08d73-316">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="08d73-317">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="08d73-317">Highlights since the last major release</span></span>
* <span data-ttu-id="08d73-318">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="08d73-318">General availability of `Az` module</span></span>
* <span data-ttu-id="08d73-319">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="08d73-319">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="08d73-320">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="08d73-320">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="08d73-321">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="08d73-321">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="08d73-322">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="08d73-322">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08d73-323">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-323">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="08d73-324">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-324">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d73-325">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d73-325">Az.Automation</span></span>
* <span data-ttu-id="08d73-326">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="08d73-326">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="08d73-327">動態分組</span><span class="sxs-lookup"><span data-stu-id="08d73-327">Dynamic grouping</span></span>
    * <span data-ttu-id="08d73-328">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="08d73-328">Pre-Post script</span></span>
    * <span data-ttu-id="08d73-329">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="08d73-329">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-330">Az.Compute</span></span>
* <span data-ttu-id="08d73-331">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-331">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="08d73-332">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="08d73-332">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d73-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d73-333">Az.KeyVault</span></span>
* <span data-ttu-id="08d73-334">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="08d73-334">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-335">Az.Network</span></span>
* <span data-ttu-id="08d73-336">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="08d73-336">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="08d73-337">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="08d73-337">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d73-338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d73-338">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d73-339">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="08d73-339">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="08d73-340">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="08d73-340">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-341">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-341">Az.Resources</span></span>
* <span data-ttu-id="08d73-342">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="08d73-342">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="08d73-343">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="08d73-343">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-344">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-344">Az.Sql</span></span>
* <span data-ttu-id="08d73-345">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="08d73-345">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d73-346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-346">Az.Storage</span></span>
* <span data-ttu-id="08d73-347">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="08d73-347">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="08d73-348">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08d73-348">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08d73-349">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08d73-349">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08d73-350">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="08d73-350">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="08d73-351">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="08d73-351">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="08d73-352">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="08d73-352">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="08d73-353">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="08d73-353">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d73-354">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-354">Az.Websites</span></span>
* <span data-ttu-id="08d73-355">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="08d73-355">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="08d73-356">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="08d73-356">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d73-357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-357">Az.Accounts</span></span>
* <span data-ttu-id="08d73-358">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-358">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="08d73-359">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="08d73-359">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d73-360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d73-360">Az.Automation</span></span>
* <span data-ttu-id="08d73-361">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-361">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="08d73-362">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="08d73-362">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="08d73-363">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="08d73-363">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d73-364">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d73-364">Az.Cdn</span></span>
* <span data-ttu-id="08d73-365">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-365">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-366">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-366">Az.Compute</span></span>
* <span data-ttu-id="08d73-367">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="08d73-367">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d73-368">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d73-368">Az.DataFactory</span></span>
* <span data-ttu-id="08d73-369">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="08d73-369">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08d73-370">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08d73-370">Az.LogicApp</span></span>
* <span data-ttu-id="08d73-371">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="08d73-371">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-372">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-372">Az.Network</span></span>
* <span data-ttu-id="08d73-373">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="08d73-373">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d73-374">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d73-374">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d73-375">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-375">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="08d73-376">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="08d73-376">SDK Update</span></span>
* <span data-ttu-id="08d73-377">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="08d73-377">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="08d73-378">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="08d73-378">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-379">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-379">Az.Resources</span></span>
* <span data-ttu-id="08d73-380">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-380">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="08d73-381">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="08d73-381">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="08d73-382">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-382">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="08d73-383">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="08d73-383">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="08d73-384">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-384">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="08d73-385">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="08d73-385">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-386">Az.Sql</span></span>
* <span data-ttu-id="08d73-387">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="08d73-387">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="08d73-388">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="08d73-388">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d73-389">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-389">Az.Storage</span></span>
* <span data-ttu-id="08d73-390">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08d73-390">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="08d73-391">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="08d73-391">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="08d73-392">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08d73-392">Az.AnalysisServices</span></span>
* <span data-ttu-id="08d73-393">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-393">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d73-394">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d73-394">Az.Automation</span></span>
* <span data-ttu-id="08d73-395">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="08d73-395">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="08d73-396">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-396">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="08d73-397">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="08d73-397">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d73-398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d73-398">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d73-399">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="08d73-399">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-400">Az.Compute</span></span>
* <span data-ttu-id="08d73-401">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="08d73-401">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="08d73-402">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="08d73-402">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="08d73-403">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-403">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="08d73-404">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="08d73-404">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d73-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d73-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d73-406">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-406">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="08d73-407">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="08d73-407">Az.EventHub</span></span>
* <span data-ttu-id="08d73-408">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="08d73-408">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="08d73-409">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d73-409">Az.KeyVault</span></span>
* <span data-ttu-id="08d73-410">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="08d73-410">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08d73-411">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08d73-411">Az.LogicApp</span></span>
* <span data-ttu-id="08d73-412">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="08d73-412">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="08d73-413">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="08d73-413">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="08d73-414">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-414">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="08d73-415">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08d73-415">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08d73-416">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08d73-416">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08d73-417">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08d73-417">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="08d73-418">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="08d73-418">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="08d73-419">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-419">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="08d73-420">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d73-420">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08d73-421">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d73-421">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08d73-422">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d73-422">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="08d73-423">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d73-423">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="08d73-424">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="08d73-424">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="08d73-425">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d73-425">Az.Monitor</span></span>
* <span data-ttu-id="08d73-426">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="08d73-426">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-427">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-427">Az.Network</span></span>
* <span data-ttu-id="08d73-428">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="08d73-428">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="08d73-429">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d73-429">Az.OperationalInsights</span></span>
* <span data-ttu-id="08d73-430">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="08d73-430">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="08d73-431">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="08d73-431">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="08d73-432">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="08d73-432">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="08d73-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-433">Az.Resources</span></span>
* <span data-ttu-id="08d73-434">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-434">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="08d73-435">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-435">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="08d73-436">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-436">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="08d73-437">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="08d73-437">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-438">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-438">Az.Sql</span></span>
* <span data-ttu-id="08d73-439">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="08d73-439">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="08d73-440">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="08d73-440">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d73-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-441">Az.Websites</span></span>
* <span data-ttu-id="08d73-442">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="08d73-442">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="08d73-443">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="08d73-443">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d73-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-444">Az.Accounts</span></span>
* <span data-ttu-id="08d73-445">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="08d73-445">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08d73-446">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08d73-446">Az.AnalysisServices</span></span>
<span data-ttu-id="08d73-447">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="08d73-447">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-448">Az.Compute</span></span>
* <span data-ttu-id="08d73-449">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-449">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="08d73-450">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="08d73-450">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="08d73-451">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="08d73-451">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d73-452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d73-452">Az.RecoveryServices</span></span>
<span data-ttu-id="08d73-453">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="08d73-453">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-454">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-454">Az.Resources</span></span>
* <span data-ttu-id="08d73-455">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="08d73-455">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="08d73-456">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="08d73-456">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="08d73-457">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-457">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="08d73-458">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="08d73-458">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-459">Az.Sql</span></span>
* <span data-ttu-id="08d73-460">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="08d73-460">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="08d73-461">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-461">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="08d73-462">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="08d73-462">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="08d73-463">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="08d73-463">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d73-464">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-464">Az.Accounts</span></span>
* <span data-ttu-id="08d73-465">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="08d73-465">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="08d73-466">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="08d73-466">Az.AnalysisServices</span></span>
* <span data-ttu-id="08d73-467">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="08d73-467">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="08d73-468">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d73-468">Az.RecoveryServices</span></span>
* <span data-ttu-id="08d73-469">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="08d73-469">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="08d73-470">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="08d73-470">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d73-471">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-471">Az.Accounts</span></span>
* <span data-ttu-id="08d73-472">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="08d73-472">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="08d73-473">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-473">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08d73-474">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="08d73-474">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="08d73-475">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="08d73-475">Az.Aks</span></span>
* <span data-ttu-id="08d73-476">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-476">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="08d73-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d73-477">Az.Automation</span></span>
* <span data-ttu-id="08d73-478">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-478">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="08d73-479">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-479">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="08d73-480">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="08d73-480">Az.Cdn</span></span>
* <span data-ttu-id="08d73-481">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-481">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-482">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-482">Az.Compute</span></span>
* <span data-ttu-id="08d73-483">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-483">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="08d73-484">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="08d73-484">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="08d73-485">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="08d73-485">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="08d73-486">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="08d73-486">Az.ContainerRegistry</span></span>
* <span data-ttu-id="08d73-487">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-487">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="08d73-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="08d73-488">Az.DataFactory</span></span>
* <span data-ttu-id="08d73-489">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="08d73-489">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d73-490">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d73-490">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d73-491">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-491">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="08d73-492">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="08d73-492">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="08d73-493">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-493">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d73-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d73-494">Az.IotHub</span></span>
* <span data-ttu-id="08d73-495">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08d73-495">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="08d73-496">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d73-496">Az.KeyVault</span></span>
* <span data-ttu-id="08d73-497">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-497">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-498">Az.Network</span></span>
* <span data-ttu-id="08d73-499">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-499">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-500">Az.Resources</span></span>
* <span data-ttu-id="08d73-501">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="08d73-501">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="08d73-502">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-502">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="08d73-503">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="08d73-503">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="08d73-504">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-504">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="08d73-505">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-505">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="08d73-506">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-506">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="08d73-507">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="08d73-507">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d73-508">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d73-508">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d73-509">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="08d73-509">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="08d73-510">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="08d73-510">Fix some error messages.</span></span>
* <span data-ttu-id="08d73-511">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="08d73-511">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="08d73-512">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="08d73-512">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08d73-513">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08d73-513">Az.SignalR</span></span>
* <span data-ttu-id="08d73-514">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-514">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-515">Az.Sql</span></span>
* <span data-ttu-id="08d73-516">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08d73-517">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="08d73-517">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="08d73-518">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-518">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="08d73-519">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="08d73-519">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d73-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-520">Az.Storage</span></span>
* <span data-ttu-id="08d73-521">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-521">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08d73-522">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="08d73-522">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="08d73-523">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="08d73-523">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="08d73-524">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="08d73-524">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="08d73-525">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="08d73-525">Az.TrafficManager</span></span>
* <span data-ttu-id="08d73-526">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-526">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d73-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-527">Az.Websites</span></span>
* <span data-ttu-id="08d73-528">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="08d73-528">Update incorrect online help URLs</span></span>
* <span data-ttu-id="08d73-529">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="08d73-529">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="08d73-530">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="08d73-530">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="08d73-531">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="08d73-531">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="08d73-532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-532">Az.Accounts</span></span>
* <span data-ttu-id="08d73-533">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="08d73-533">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-534">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-534">Az.Compute</span></span>
* <span data-ttu-id="08d73-535">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="08d73-535">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="08d73-536">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="08d73-536">Updated the description of ID in help files</span></span>
* <span data-ttu-id="08d73-537">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="08d73-537">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d73-538">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d73-538">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d73-539">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="08d73-539">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="08d73-540">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="08d73-540">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="08d73-541">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="08d73-541">Az.EventGrid</span></span>
* <span data-ttu-id="08d73-542">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="08d73-542">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="08d73-543">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="08d73-543">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="08d73-544">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="08d73-544">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="08d73-545">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="08d73-545">Event Time-To-Live,</span></span>
        - <span data-ttu-id="08d73-546">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="08d73-546">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="08d73-547">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="08d73-547">Dead letter endpoint.</span></span>
    - <span data-ttu-id="08d73-548">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="08d73-548">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="08d73-549">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="08d73-549">Event Time-To-Live,</span></span>
        - <span data-ttu-id="08d73-550">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="08d73-550">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="08d73-551">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="08d73-551">Dead letter endpoint.</span></span>
* <span data-ttu-id="08d73-552">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="08d73-552">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="08d73-553">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="08d73-553">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="08d73-554">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="08d73-554">Az.IotHub</span></span>
* <span data-ttu-id="08d73-555">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="08d73-555">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="08d73-556">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="08d73-556">Az.LogicApp</span></span>
* <span data-ttu-id="08d73-557">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="08d73-557">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-558">Az.Resources</span></span>
* <span data-ttu-id="08d73-559">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="08d73-559">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="08d73-560">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="08d73-560">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="08d73-561">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="08d73-561">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="08d73-562">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="08d73-562">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="08d73-563">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="08d73-563">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="08d73-564">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="08d73-564">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="08d73-565">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="08d73-565">Az.SignalR</span></span>
* <span data-ttu-id="08d73-566">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="08d73-566">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-567">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-567">Az.Sql</span></span>
* <span data-ttu-id="08d73-568">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="08d73-568">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="08d73-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-569">Az.Storage</span></span>
* <span data-ttu-id="08d73-570">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="08d73-570">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="08d73-571">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="08d73-571">New-AzStorageContext</span></span>
* <span data-ttu-id="08d73-572">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="08d73-572">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="08d73-573">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="08d73-573">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d73-574">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-574">Az.Websites</span></span>
* <span data-ttu-id="08d73-575">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="08d73-575">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="08d73-576">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="08d73-576">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="08d73-577">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="08d73-577">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="08d73-578">一般</span><span class="sxs-lookup"><span data-stu-id="08d73-578">General</span></span>

- <span data-ttu-id="08d73-579">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="08d73-579">General Availability of Az Module</span></span>
- <span data-ttu-id="08d73-580">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="08d73-580">Online help for each module</span></span>
- <span data-ttu-id="08d73-581">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="08d73-581">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="08d73-582">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-582">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="08d73-583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-583">Az.Accounts</span></span>
- <span data-ttu-id="08d73-584">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="08d73-584">Changed from Az.Profile</span></span>
- <span data-ttu-id="08d73-585">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="08d73-585">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="08d73-586">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d73-586">Az.ApiManagement</span></span>
- <span data-ttu-id="08d73-587">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="08d73-587">Fixes for #7002</span></span>
- <span data-ttu-id="08d73-588">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="08d73-589">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="08d73-589">Az.Batch</span></span>
- <span data-ttu-id="08d73-590">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="08d73-590">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="08d73-591">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="08d73-591">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="08d73-592">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="08d73-593">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="08d73-593">Az.Billing</span></span>
- <span data-ttu-id="08d73-594">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-594">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="08d73-595">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="08d73-595">Az.CognitivServices</span></span>
- <span data-ttu-id="08d73-596">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="08d73-596">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="08d73-597">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="08d73-597">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="08d73-598">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08d73-598">Az.ContainerInstance</span></span>
- <span data-ttu-id="08d73-599">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="08d73-599">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="08d73-600">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="08d73-600">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="08d73-601">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-601">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="08d73-602">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d73-602">Az.DataLakeStore</span></span>
- <span data-ttu-id="08d73-603">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="08d73-604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="08d73-604">Az.Monitor</span></span>
- <span data-ttu-id="08d73-605">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-605">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="08d73-606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="08d73-606">Az.KeyVault</span></span>
- <span data-ttu-id="08d73-607">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="08d73-607">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="08d73-608">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="08d73-608">Az.MachineLearning</span></span>
- <span data-ttu-id="08d73-609">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-609">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="08d73-610">Az.Media</span><span class="sxs-lookup"><span data-stu-id="08d73-610">Az.Media</span></span>
- <span data-ttu-id="08d73-611">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="08d73-611">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="08d73-612">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-612">Az.Network</span></span>
<span data-ttu-id="08d73-613">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-613">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="08d73-614">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="08d73-614">New cmdlets added:</span></span>
        - <span data-ttu-id="08d73-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d73-615">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d73-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d73-616">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d73-617">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d73-617">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d73-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d73-618">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d73-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d73-619">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="08d73-620">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="08d73-620">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="08d73-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="08d73-621">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="08d73-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="08d73-622">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="08d73-623">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="08d73-623">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="08d73-624">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08d73-624">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="08d73-625">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="08d73-625">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="08d73-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="08d73-626">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="08d73-627">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08d73-627">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="08d73-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="08d73-628">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="08d73-629">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="08d73-629">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="08d73-630">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-630">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="08d73-631">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08d73-631">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="08d73-632">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08d73-632">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="08d73-633">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="08d73-633">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="08d73-634">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-634">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="08d73-635">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-635">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="08d73-636">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="08d73-636">Az.OperationalInsights</span></span>
- <span data-ttu-id="08d73-637">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-637">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="08d73-638">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08d73-638">Az.Profile</span></span>
- <span data-ttu-id="08d73-639">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="08d73-639">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="08d73-640">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d73-640">Az.RecoveryServices</span></span>
- <span data-ttu-id="08d73-641">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-641">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="08d73-642">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-642">Az.Resources</span></span>
- <span data-ttu-id="08d73-643">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-643">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="08d73-644">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d73-644">Az.ServiceFabric</span></span>
- <span data-ttu-id="08d73-645">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="08d73-645">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="08d73-646">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-646">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="08d73-647">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="08d73-647">Az.SIgnalR</span></span>
- <span data-ttu-id="08d73-648">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="08d73-648">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="08d73-649">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-649">Az.Sql</span></span>
- <span data-ttu-id="08d73-650">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="08d73-650">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="08d73-651">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="08d73-651">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="08d73-652">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="08d73-653">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-653">Az.Storage</span></span>
- <span data-ttu-id="08d73-654">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="08d73-655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-655">Az.Websites</span></span>
- <span data-ttu-id="08d73-656">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="08d73-656">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="08d73-657">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="08d73-657">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="08d73-658">一般</span><span class="sxs-lookup"><span data-stu-id="08d73-658">General</span></span>

* <span data-ttu-id="08d73-659">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="08d73-659">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="08d73-660">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-660">Az.Compute</span></span>

* <span data-ttu-id="08d73-661">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="08d73-661">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="08d73-662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d73-662">Az.DataLakeStore</span></span>

* <span data-ttu-id="08d73-663">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="08d73-663">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="08d73-664">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="08d73-664">Az.FrontDoor</span></span>

* <span data-ttu-id="08d73-665">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="08d73-665">Fixed some broken links</span></span>
    - <span data-ttu-id="08d73-666">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="08d73-666">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="08d73-667">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="08d73-667">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="08d73-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="08d73-668">Az.RecoveryServices</span></span>

* <span data-ttu-id="08d73-669">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="08d73-669">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="08d73-670">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="08d73-670">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="08d73-671">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-671">Az.Resources</span></span>

* <span data-ttu-id="08d73-672">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="08d73-672">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="08d73-673">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="08d73-673">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="08d73-674">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-674">Az.Sql</span></span>

* <span data-ttu-id="08d73-675">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="08d73-675">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="08d73-676">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-676">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="08d73-677">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="08d73-677">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="08d73-678">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-678">Az.Storage</span></span>

* <span data-ttu-id="08d73-679">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="08d73-679">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="08d73-680">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="08d73-680">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="08d73-681">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="08d73-681">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="08d73-682">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="08d73-682">Support Static Website configuration</span></span>
    - <span data-ttu-id="08d73-683">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08d73-683">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="08d73-684">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="08d73-684">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="08d73-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-685">Az.Websites</span></span>

* <span data-ttu-id="08d73-686">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08d73-686">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="08d73-687">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="08d73-687">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="08d73-688">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="08d73-688">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="08d73-689">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="08d73-689">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="08d73-690">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="08d73-690">Az.ApiManagement</span></span>
* <span data-ttu-id="08d73-691">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="08d73-691">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="08d73-692">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="08d73-692">Az.Automation</span></span>
* <span data-ttu-id="08d73-693">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-693">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="08d73-694">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-694">Added Update Management cmdlets</span></span>
* <span data-ttu-id="08d73-695">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-695">Added Source Control cmdlets</span></span>
* <span data-ttu-id="08d73-696">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-696">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="08d73-697">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="08d73-697">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="08d73-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-698">Az.Compute</span></span>
* <span data-ttu-id="08d73-699">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="08d73-699">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="08d73-700">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="08d73-700">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="08d73-701">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="08d73-701">Az.ContainerInstance</span></span>
* <span data-ttu-id="08d73-702">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="08d73-702">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="08d73-703">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="08d73-703">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="08d73-704">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="08d73-704">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="08d73-705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-705">Az.Network</span></span>
* <span data-ttu-id="08d73-706">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="08d73-706">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="08d73-707">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="08d73-707">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="08d73-708">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="08d73-708">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="08d73-709">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="08d73-709">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="08d73-710">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="08d73-710">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="08d73-711">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="08d73-711">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="08d73-712">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="08d73-712">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="08d73-713">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="08d73-713">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="08d73-714">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="08d73-714">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="08d73-715">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="08d73-715">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="08d73-716">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="08d73-716">Az.Relay</span></span>
* <span data-ttu-id="08d73-717">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="08d73-717">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="08d73-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-718">Az.Resources</span></span>
* <span data-ttu-id="08d73-719">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="08d73-719">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="08d73-720">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="08d73-720">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="08d73-721">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="08d73-721">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="08d73-722">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d73-722">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d73-723">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="08d73-723">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="08d73-724">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-724">Az.Sql</span></span>
* <span data-ttu-id="08d73-725">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-725">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="08d73-726">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08d73-726">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08d73-727">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08d73-727">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08d73-728">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08d73-728">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08d73-729">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="08d73-729">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="08d73-730">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08d73-730">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08d73-731">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08d73-731">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08d73-732">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08d73-732">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="08d73-733">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="08d73-733">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="08d73-734">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="08d73-734">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="08d73-735">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="08d73-735">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="08d73-736">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="08d73-736">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="08d73-737">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="08d73-737">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="08d73-738">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="08d73-738">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="08d73-739">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="08d73-739">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="08d73-740">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="08d73-740">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="08d73-741">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-741">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="08d73-742">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="08d73-742">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="08d73-743">一般</span><span class="sxs-lookup"><span data-stu-id="08d73-743">General</span></span>
* <span data-ttu-id="08d73-744">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="08d73-744">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="08d73-745">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08d73-745">Az.Profile</span></span>
* <span data-ttu-id="08d73-746">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="08d73-746">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="08d73-747">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="08d73-747">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="08d73-748">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="08d73-748">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="08d73-749">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="08d73-749">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="08d73-750">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-750">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="08d73-751">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-751">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="08d73-752">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-752">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="08d73-753">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d73-753">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d73-754">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="08d73-754">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-755">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-755">Az.Compute</span></span>
* <span data-ttu-id="08d73-756">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-756">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="08d73-757">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="08d73-757">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="08d73-758">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="08d73-758">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d73-759">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d73-759">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d73-760">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="08d73-760">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="08d73-761">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="08d73-761">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="08d73-762">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="08d73-762">Az.Insights</span></span>
* <span data-ttu-id="08d73-763">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="08d73-763">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="08d73-764">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="08d73-764">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="08d73-765">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="08d73-765">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="08d73-766">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="08d73-766">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-767">Az.Network</span></span>
* <span data-ttu-id="08d73-768">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="08d73-768">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="08d73-769">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="08d73-769">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="08d73-770">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="08d73-770">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="08d73-771">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="08d73-771">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="08d73-772">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="08d73-772">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="08d73-773">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="08d73-773">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="08d73-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="08d73-774">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="08d73-775">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="08d73-775">Az.PolicyInsights</span></span>
* <span data-ttu-id="08d73-776">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-776">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-777">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-777">Az.Resources</span></span>
* <span data-ttu-id="08d73-778">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="08d73-778">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="08d73-779">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="08d73-779">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="08d73-780">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="08d73-780">Az.ServiceBus</span></span>
* <span data-ttu-id="08d73-781">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="08d73-781">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="08d73-782">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="08d73-782">Az.ServiceFabric</span></span>
* <span data-ttu-id="08d73-783">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="08d73-783">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="08d73-784">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="08d73-784">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="08d73-785">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="08d73-785">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="08d73-786">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="08d73-786">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="08d73-787">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="08d73-787">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="08d73-788">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="08d73-788">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="08d73-789">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="08d73-789">Az.Profile</span></span>
* <span data-ttu-id="08d73-790">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-790">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="08d73-791">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="08d73-791">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-792">Az.Compute</span></span>
* <span data-ttu-id="08d73-793">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="08d73-793">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="08d73-794">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08d73-794">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="08d73-795">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="08d73-795">Az.DataLakeStore</span></span>
* <span data-ttu-id="08d73-796">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="08d73-796">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="08d73-797">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="08d73-797">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="08d73-798">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="08d73-798">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="08d73-799">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="08d73-799">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="08d73-800">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="08d73-800">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-801">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-801">Az.Network</span></span>
* <span data-ttu-id="08d73-802">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="08d73-802">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="08d73-803">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08d73-803">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-804">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-804">Az.Resources</span></span>
* <span data-ttu-id="08d73-805">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="08d73-805">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="08d73-806">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="08d73-806">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="08d73-807">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="08d73-807">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="08d73-808">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="08d73-808">Azure.Storage</span></span>
* <span data-ttu-id="08d73-809">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-809">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="08d73-810">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="08d73-810">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="08d73-811">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="08d73-811">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="08d73-812">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="08d73-812">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="08d73-813">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="08d73-813">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="08d73-814">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="08d73-814">Az.CognitiveServices</span></span>
* <span data-ttu-id="08d73-815">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="08d73-815">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="08d73-816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="08d73-816">Az.Compute</span></span>
* <span data-ttu-id="08d73-817">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="08d73-817">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="08d73-818">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="08d73-818">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="08d73-819">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="08d73-819">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="08d73-820">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="08d73-820">Az.DataFactoryV2</span></span>
* <span data-ttu-id="08d73-821">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="08d73-821">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="08d73-822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="08d73-822">Az.Network</span></span>
* <span data-ttu-id="08d73-823">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="08d73-823">Added NetworkProfile functionality.</span></span> <span data-ttu-id="08d73-824">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-824">new cmdlets added</span></span>
    - <span data-ttu-id="08d73-825">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08d73-825">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="08d73-826">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08d73-826">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="08d73-827">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08d73-827">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="08d73-828">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="08d73-828">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="08d73-829">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="08d73-829">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="08d73-830">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="08d73-830">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="08d73-831">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="08d73-831">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="08d73-832">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-832">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="08d73-833">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="08d73-833">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="08d73-834">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="08d73-834">Az.RedisCache</span></span>
* <span data-ttu-id="08d73-835">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="08d73-835">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="08d73-836">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="08d73-836">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="08d73-837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="08d73-837">Az.Resources</span></span>
* <span data-ttu-id="08d73-838">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="08d73-838">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="08d73-839">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="08d73-839">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="08d73-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="08d73-840">Az.Sql</span></span>
* <span data-ttu-id="08d73-841">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="08d73-841">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="08d73-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="08d73-842">Az.Websites</span></span>
* <span data-ttu-id="08d73-843">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="08d73-843">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="08d73-844">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="08d73-844">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="08d73-845">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="08d73-845">0.2.0 - September 2018</span></span>
 <span data-ttu-id="08d73-846">初始版本</span><span class="sxs-lookup"><span data-stu-id="08d73-846">Initial Release</span></span>