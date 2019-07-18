---
ms.openlocfilehash: ffeba2cff2e157e7ec0fb7639f9d4075c359c85e
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863830"
---
## <a name="180---april-2019"></a><span data-ttu-id="26c59-101">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="26c59-101">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="26c59-102">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="26c59-102">Highlights since the last major release</span></span>
* <span data-ttu-id="26c59-103">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="26c59-103">General availability of `Az` module</span></span>
* <span data-ttu-id="26c59-104">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="26c59-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="26c59-105">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="26c59-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="26c59-106">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="26c59-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="26c59-107">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="26c59-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="26c59-108">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="26c59-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="26c59-109">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="26c59-110">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-110">Az.Accounts</span></span>
* <span data-ttu-id="26c59-111">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="26c59-111">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="26c59-112">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="26c59-112">Az.Batch</span></span>
* <span data-ttu-id="26c59-113">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-113">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="26c59-114">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="26c59-114">Az.Cdn</span></span>
* <span data-ttu-id="26c59-115">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="26c59-116">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="26c59-116">Az.CognitiveServices</span></span>
* <span data-ttu-id="26c59-117">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-118">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-118">Az.Compute</span></span>
* <span data-ttu-id="26c59-119">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="26c59-119">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="26c59-120">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="26c59-121">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="26c59-121">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="26c59-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="26c59-122">Az.DataFactory</span></span>
* <span data-ttu-id="26c59-123">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="26c59-123">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="26c59-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26c59-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="26c59-125">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-125">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="26c59-126">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="26c59-126">Az.EventGrid</span></span>
* <span data-ttu-id="26c59-127">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26c59-127">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="26c59-128">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="26c59-128">Az.EventHub</span></span>
* <span data-ttu-id="26c59-129">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-129">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="26c59-130">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="26c59-130">Az.HDInsight</span></span>
* <span data-ttu-id="26c59-131">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-131">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="26c59-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="26c59-132">Az.IotHub</span></span>
* <span data-ttu-id="26c59-133">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="26c59-134">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="26c59-134">Az.KeyVault</span></span>
* <span data-ttu-id="26c59-135">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="26c59-136">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="26c59-136">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="26c59-137">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="26c59-137">Az.MachineLearning</span></span>
* <span data-ttu-id="26c59-138">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="26c59-139">Az.Media</span><span class="sxs-lookup"><span data-stu-id="26c59-139">Az.Media</span></span>
* <span data-ttu-id="26c59-140">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="26c59-141">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="26c59-141">Az.Monitor</span></span>
  * <span data-ttu-id="26c59-142">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-142">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="26c59-143">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="26c59-143">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="26c59-144">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="26c59-144">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="26c59-145">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="26c59-145">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="26c59-146">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="26c59-146">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="26c59-147">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="26c59-147">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="26c59-148">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="26c59-148">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="26c59-149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-149">Az.Network</span></span>
* <span data-ttu-id="26c59-150">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-150">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="26c59-151">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="26c59-151">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="26c59-152">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="26c59-152">Az.NotificationHubs</span></span>
* <span data-ttu-id="26c59-153">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="26c59-154">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="26c59-154">Az.OperationalInsights</span></span>
* <span data-ttu-id="26c59-155">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="26c59-156">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="26c59-156">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="26c59-157">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="26c59-158">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="26c59-158">Az.RecoveryServices</span></span>
* <span data-ttu-id="26c59-159">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="26c59-160">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="26c59-160">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="26c59-161">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="26c59-161">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="26c59-162">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="26c59-162">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="26c59-163">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="26c59-163">Az.RedisCache</span></span>
* <span data-ttu-id="26c59-164">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-165">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-165">Az.Resources</span></span>
* <span data-ttu-id="26c59-166">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="26c59-166">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-167">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-167">Az.Sql</span></span>
* <span data-ttu-id="26c59-168">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="26c59-168">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="26c59-169">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-169">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="26c59-170">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="26c59-170">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="26c59-171">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="26c59-171">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="26c59-172">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="26c59-172">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="26c59-173">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="26c59-173">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="26c59-174">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="26c59-174">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="26c59-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="26c59-175">Az.Websites</span></span>
* <span data-ttu-id="26c59-176">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="26c59-176">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="26c59-177">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="26c59-178">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="26c59-178">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="26c59-179">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="26c59-179">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="26c59-180">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="26c59-180">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="26c59-181">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="26c59-181">Highlights since the last major release</span></span>
* <span data-ttu-id="26c59-182">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="26c59-182">General availability of `Az` module</span></span>
* <span data-ttu-id="26c59-183">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="26c59-183">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="26c59-184">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="26c59-184">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="26c59-185">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="26c59-185">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="26c59-186">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="26c59-186">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="26c59-187">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="26c59-187">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="26c59-188">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-188">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="26c59-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-189">Az.Accounts</span></span>
* <span data-ttu-id="26c59-190">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="26c59-190">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="26c59-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="26c59-191">Az.AnalysisServices</span></span>
* <span data-ttu-id="26c59-192">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="26c59-192">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="26c59-193">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="26c59-193">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="26c59-194">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="26c59-194">Az.Automation</span></span>
* <span data-ttu-id="26c59-195">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="26c59-195">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="26c59-196">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="26c59-196">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="26c59-197">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="26c59-197">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-198">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-198">Az.Compute</span></span>
* <span data-ttu-id="26c59-199">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="26c59-199">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="26c59-200">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="26c59-200">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="26c59-201">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="26c59-201">Az.ContainerInstance</span></span>
* <span data-ttu-id="26c59-202">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="26c59-202">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="26c59-203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="26c59-203">Az.DataFactory</span></span>
* <span data-ttu-id="26c59-204">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="26c59-204">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="26c59-205">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26c59-205">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-206">Az.Resources</span></span>
* <span data-ttu-id="26c59-207">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="26c59-207">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="26c59-208">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="26c59-208">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="26c59-209">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="26c59-209">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="26c59-210">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="26c59-210">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="26c59-211">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="26c59-211">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="26c59-212">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="26c59-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-213">Az.Sql</span></span>
* <span data-ttu-id="26c59-214">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="26c59-214">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="26c59-215">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="26c59-215">Az.Storage</span></span>
* <span data-ttu-id="26c59-216">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="26c59-216">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="26c59-217">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="26c59-217">New-AzStorageContext</span></span>
* <span data-ttu-id="26c59-218">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="26c59-218">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="26c59-219">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="26c59-219">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="26c59-220">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="26c59-220">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="26c59-221">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="26c59-221">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="26c59-222">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="26c59-222">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="26c59-223">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-223">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="26c59-224">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="26c59-224">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="26c59-225">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="26c59-225">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="26c59-226">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="26c59-226">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="26c59-227">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="26c59-227">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="26c59-228">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="26c59-228">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="26c59-229">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="26c59-229">Highlights since the last major release</span></span>
* <span data-ttu-id="26c59-230">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="26c59-230">General availability of `Az` module</span></span>
* <span data-ttu-id="26c59-231">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="26c59-231">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="26c59-232">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="26c59-232">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="26c59-233">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="26c59-233">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="26c59-234">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="26c59-234">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="26c59-235">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="26c59-235">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="26c59-236">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-236">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="26c59-237">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="26c59-237">Az.Automation</span></span>
* <span data-ttu-id="26c59-238">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="26c59-238">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="26c59-239">動態分組</span><span class="sxs-lookup"><span data-stu-id="26c59-239">Dynamic grouping</span></span>
    * <span data-ttu-id="26c59-240">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="26c59-240">Pre-Post script</span></span>
    * <span data-ttu-id="26c59-241">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="26c59-241">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-242">Az.Compute</span></span>
* <span data-ttu-id="26c59-243">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-243">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="26c59-244">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="26c59-244">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="26c59-245">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="26c59-245">Az.KeyVault</span></span>
* <span data-ttu-id="26c59-246">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="26c59-246">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="26c59-247">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-247">Az.Network</span></span>
* <span data-ttu-id="26c59-248">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="26c59-248">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="26c59-249">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="26c59-249">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="26c59-250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="26c59-250">Az.RecoveryServices</span></span>
* <span data-ttu-id="26c59-251">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="26c59-251">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="26c59-252">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="26c59-252">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-253">Az.Resources</span></span>
* <span data-ttu-id="26c59-254">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="26c59-254">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="26c59-255">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="26c59-255">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-256">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-256">Az.Sql</span></span>
* <span data-ttu-id="26c59-257">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="26c59-257">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="26c59-258">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="26c59-258">Az.Storage</span></span>
* <span data-ttu-id="26c59-259">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="26c59-259">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="26c59-260">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="26c59-260">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="26c59-261">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="26c59-261">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="26c59-262">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="26c59-262">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="26c59-263">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="26c59-263">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="26c59-264">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="26c59-264">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="26c59-265">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="26c59-265">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="26c59-266">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="26c59-266">Az.Websites</span></span>
* <span data-ttu-id="26c59-267">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="26c59-267">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="26c59-268">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="26c59-268">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="26c59-269">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-269">Az.Accounts</span></span>
* <span data-ttu-id="26c59-270">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-270">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="26c59-271">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="26c59-271">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="26c59-272">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="26c59-272">Az.Automation</span></span>
* <span data-ttu-id="26c59-273">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-273">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="26c59-274">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="26c59-274">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="26c59-275">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="26c59-275">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="26c59-276">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="26c59-276">Az.Cdn</span></span>
* <span data-ttu-id="26c59-277">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-277">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-278">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-278">Az.Compute</span></span>
* <span data-ttu-id="26c59-279">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="26c59-279">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="26c59-280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="26c59-280">Az.DataFactory</span></span>
* <span data-ttu-id="26c59-281">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="26c59-281">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="26c59-282">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="26c59-282">Az.LogicApp</span></span>
* <span data-ttu-id="26c59-283">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="26c59-283">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="26c59-284">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-284">Az.Network</span></span>
* <span data-ttu-id="26c59-285">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="26c59-285">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="26c59-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="26c59-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="26c59-287">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="26c59-287">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="26c59-288">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="26c59-288">SDK Update</span></span>
* <span data-ttu-id="26c59-289">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="26c59-289">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="26c59-290">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="26c59-290">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-291">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-291">Az.Resources</span></span>
* <span data-ttu-id="26c59-292">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-292">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="26c59-293">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="26c59-293">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="26c59-294">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-294">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="26c59-295">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="26c59-295">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="26c59-296">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-296">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="26c59-297">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="26c59-297">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-298">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-298">Az.Sql</span></span>
* <span data-ttu-id="26c59-299">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="26c59-299">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="26c59-300">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="26c59-300">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="26c59-301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="26c59-301">Az.Storage</span></span>
* <span data-ttu-id="26c59-302">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26c59-302">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="26c59-303">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="26c59-303">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="26c59-304">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="26c59-304">Az.AnalysisServices</span></span>
* <span data-ttu-id="26c59-305">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-305">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="26c59-306">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="26c59-306">Az.Automation</span></span>
* <span data-ttu-id="26c59-307">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="26c59-307">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="26c59-308">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-308">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="26c59-309">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="26c59-309">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="26c59-310">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="26c59-310">Az.CognitiveServices</span></span>
* <span data-ttu-id="26c59-311">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="26c59-311">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-312">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-312">Az.Compute</span></span>
* <span data-ttu-id="26c59-313">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="26c59-313">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="26c59-314">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="26c59-314">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="26c59-315">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-315">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="26c59-316">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="26c59-316">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="26c59-317">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26c59-317">Az.DataLakeStore</span></span>
* <span data-ttu-id="26c59-318">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-318">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="26c59-319">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="26c59-319">Az.EventHub</span></span>
* <span data-ttu-id="26c59-320">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="26c59-320">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="26c59-321">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="26c59-321">Az.KeyVault</span></span>
* <span data-ttu-id="26c59-322">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="26c59-322">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="26c59-323">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="26c59-323">Az.LogicApp</span></span>
* <span data-ttu-id="26c59-324">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="26c59-324">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="26c59-325">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="26c59-325">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="26c59-326">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-326">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="26c59-327">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="26c59-327">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="26c59-328">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="26c59-328">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="26c59-329">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="26c59-329">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="26c59-330">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="26c59-330">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="26c59-331">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-331">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="26c59-332">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="26c59-332">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="26c59-333">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="26c59-333">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="26c59-334">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="26c59-334">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="26c59-335">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="26c59-335">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="26c59-336">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="26c59-336">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="26c59-337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="26c59-337">Az.Monitor</span></span>
* <span data-ttu-id="26c59-338">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="26c59-338">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="26c59-339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-339">Az.Network</span></span>
* <span data-ttu-id="26c59-340">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="26c59-340">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="26c59-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="26c59-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="26c59-342">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="26c59-342">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="26c59-343">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="26c59-343">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="26c59-344">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="26c59-344">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="26c59-345">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-345">Az.Resources</span></span>
* <span data-ttu-id="26c59-346">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-346">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="26c59-347">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-347">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="26c59-348">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-348">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="26c59-349">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="26c59-349">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-350">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-350">Az.Sql</span></span>
* <span data-ttu-id="26c59-351">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="26c59-351">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="26c59-352">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="26c59-352">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="26c59-353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="26c59-353">Az.Websites</span></span>
* <span data-ttu-id="26c59-354">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="26c59-354">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="26c59-355">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="26c59-355">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="26c59-356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-356">Az.Accounts</span></span>
* <span data-ttu-id="26c59-357">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="26c59-357">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="26c59-358">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="26c59-358">Az.AnalysisServices</span></span>
<span data-ttu-id="26c59-359">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="26c59-359">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-360">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-360">Az.Compute</span></span>
* <span data-ttu-id="26c59-361">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="26c59-361">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="26c59-362">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="26c59-362">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="26c59-363">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="26c59-363">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="26c59-364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="26c59-364">Az.RecoveryServices</span></span>
<span data-ttu-id="26c59-365">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="26c59-365">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-366">Az.Resources</span></span>
* <span data-ttu-id="26c59-367">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="26c59-367">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="26c59-368">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="26c59-368">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="26c59-369">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-369">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="26c59-370">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="26c59-370">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-371">Az.Sql</span></span>
* <span data-ttu-id="26c59-372">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="26c59-372">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="26c59-373">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-373">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="26c59-374">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="26c59-374">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="26c59-375">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="26c59-375">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="26c59-376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-376">Az.Accounts</span></span>
* <span data-ttu-id="26c59-377">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="26c59-377">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="26c59-378">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="26c59-378">Az.AnalysisServices</span></span>
* <span data-ttu-id="26c59-379">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="26c59-379">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="26c59-380">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="26c59-380">Az.RecoveryServices</span></span>
* <span data-ttu-id="26c59-381">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="26c59-381">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="26c59-382">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="26c59-382">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="26c59-383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-383">Az.Accounts</span></span>
* <span data-ttu-id="26c59-384">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="26c59-384">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="26c59-385">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-385">Update incorrect online help URLs</span></span>
* <span data-ttu-id="26c59-386">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="26c59-386">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="26c59-387">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="26c59-387">Az.Aks</span></span>
* <span data-ttu-id="26c59-388">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-388">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="26c59-389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="26c59-389">Az.Automation</span></span>
* <span data-ttu-id="26c59-390">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="26c59-390">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="26c59-391">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-391">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="26c59-392">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="26c59-392">Az.Cdn</span></span>
* <span data-ttu-id="26c59-393">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-393">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-394">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-394">Az.Compute</span></span>
* <span data-ttu-id="26c59-395">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-395">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="26c59-396">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="26c59-396">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="26c59-397">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="26c59-397">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="26c59-398">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="26c59-398">Az.ContainerRegistry</span></span>
* <span data-ttu-id="26c59-399">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-399">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="26c59-400">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="26c59-400">Az.DataFactory</span></span>
* <span data-ttu-id="26c59-401">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="26c59-401">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="26c59-402">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26c59-402">Az.DataLakeStore</span></span>
* <span data-ttu-id="26c59-403">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-403">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="26c59-404">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="26c59-404">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="26c59-405">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-405">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="26c59-406">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="26c59-406">Az.IotHub</span></span>
* <span data-ttu-id="26c59-407">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26c59-407">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="26c59-408">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="26c59-408">Az.KeyVault</span></span>
* <span data-ttu-id="26c59-409">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-409">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="26c59-410">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-410">Az.Network</span></span>
* <span data-ttu-id="26c59-411">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-411">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-412">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-412">Az.Resources</span></span>
* <span data-ttu-id="26c59-413">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="26c59-413">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="26c59-414">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-414">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="26c59-415">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="26c59-415">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="26c59-416">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-416">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="26c59-417">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-417">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="26c59-418">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-418">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="26c59-419">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="26c59-419">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="26c59-420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="26c59-420">Az.ServiceFabric</span></span>
* <span data-ttu-id="26c59-421">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="26c59-421">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="26c59-422">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="26c59-422">Fix some error messages.</span></span>
* <span data-ttu-id="26c59-423">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="26c59-423">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="26c59-424">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="26c59-424">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="26c59-425">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="26c59-425">Az.SignalR</span></span>
* <span data-ttu-id="26c59-426">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-426">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-427">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-427">Az.Sql</span></span>
* <span data-ttu-id="26c59-428">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-428">Update incorrect online help URLs</span></span>
* <span data-ttu-id="26c59-429">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="26c59-429">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="26c59-430">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-430">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="26c59-431">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="26c59-431">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="26c59-432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="26c59-432">Az.Storage</span></span>
* <span data-ttu-id="26c59-433">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-433">Update incorrect online help URLs</span></span>
* <span data-ttu-id="26c59-434">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="26c59-434">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="26c59-435">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="26c59-435">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="26c59-436">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="26c59-436">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="26c59-437">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="26c59-437">Az.TrafficManager</span></span>
* <span data-ttu-id="26c59-438">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-438">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="26c59-439">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="26c59-439">Az.Websites</span></span>
* <span data-ttu-id="26c59-440">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="26c59-440">Update incorrect online help URLs</span></span>
* <span data-ttu-id="26c59-441">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="26c59-441">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="26c59-442">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="26c59-442">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="26c59-443">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="26c59-443">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="26c59-444">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-444">Az.Accounts</span></span>
* <span data-ttu-id="26c59-445">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="26c59-445">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-446">Az.Compute</span></span>
* <span data-ttu-id="26c59-447">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="26c59-447">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="26c59-448">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="26c59-448">Updated the description of ID in help files</span></span>
* <span data-ttu-id="26c59-449">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="26c59-449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="26c59-450">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26c59-450">Az.DataLakeStore</span></span>
* <span data-ttu-id="26c59-451">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="26c59-451">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="26c59-452">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="26c59-452">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="26c59-453">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="26c59-453">Az.EventGrid</span></span>
* <span data-ttu-id="26c59-454">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="26c59-454">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="26c59-455">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="26c59-455">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="26c59-456">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="26c59-456">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="26c59-457">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="26c59-457">Event Time-To-Live,</span></span>
        - <span data-ttu-id="26c59-458">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="26c59-458">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="26c59-459">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="26c59-459">Dead letter endpoint.</span></span>
    - <span data-ttu-id="26c59-460">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="26c59-460">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="26c59-461">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="26c59-461">Event Time-To-Live,</span></span>
        - <span data-ttu-id="26c59-462">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="26c59-462">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="26c59-463">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="26c59-463">Dead letter endpoint.</span></span>
* <span data-ttu-id="26c59-464">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="26c59-464">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="26c59-465">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="26c59-465">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="26c59-466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="26c59-466">Az.IotHub</span></span>
* <span data-ttu-id="26c59-467">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="26c59-467">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="26c59-468">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="26c59-468">Az.LogicApp</span></span>
* <span data-ttu-id="26c59-469">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="26c59-469">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-470">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-470">Az.Resources</span></span>
* <span data-ttu-id="26c59-471">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="26c59-471">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="26c59-472">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="26c59-472">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="26c59-473">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="26c59-473">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="26c59-474">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="26c59-474">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="26c59-475">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="26c59-475">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="26c59-476">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="26c59-476">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="26c59-477">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="26c59-477">Az.SignalR</span></span>
* <span data-ttu-id="26c59-478">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="26c59-478">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-479">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-479">Az.Sql</span></span>
* <span data-ttu-id="26c59-480">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="26c59-480">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="26c59-481">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="26c59-481">Az.Storage</span></span>
* <span data-ttu-id="26c59-482">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="26c59-482">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="26c59-483">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="26c59-483">New-AzStorageContext</span></span>
* <span data-ttu-id="26c59-484">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="26c59-484">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="26c59-485">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="26c59-485">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="26c59-486">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="26c59-486">Az.Websites</span></span>
* <span data-ttu-id="26c59-487">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="26c59-487">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="26c59-488">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="26c59-488">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="26c59-489">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="26c59-489">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="26c59-490">一般</span><span class="sxs-lookup"><span data-stu-id="26c59-490">General</span></span>

- <span data-ttu-id="26c59-491">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="26c59-491">General Availability of Az Module</span></span>
- <span data-ttu-id="26c59-492">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="26c59-492">Online help for each module</span></span>
- <span data-ttu-id="26c59-493">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="26c59-493">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="26c59-494">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-494">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="26c59-495">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-495">Az.Accounts</span></span>
- <span data-ttu-id="26c59-496">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="26c59-496">Changed from Az.Profile</span></span>
- <span data-ttu-id="26c59-497">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="26c59-497">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="26c59-498">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="26c59-498">Az.ApiManagement</span></span>
- <span data-ttu-id="26c59-499">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="26c59-499">Fixes for #7002</span></span>
- <span data-ttu-id="26c59-500">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-500">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="26c59-501">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="26c59-501">Az.Batch</span></span>
- <span data-ttu-id="26c59-502">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="26c59-502">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="26c59-503">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="26c59-503">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="26c59-504">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-504">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="26c59-505">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="26c59-505">Az.Billing</span></span>
- <span data-ttu-id="26c59-506">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-506">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="26c59-507">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="26c59-507">Az.CognitivServices</span></span>
- <span data-ttu-id="26c59-508">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="26c59-508">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="26c59-509">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="26c59-509">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="26c59-510">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="26c59-510">Az.ContainerInstance</span></span>
- <span data-ttu-id="26c59-511">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="26c59-511">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="26c59-512">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="26c59-512">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="26c59-513">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-513">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="26c59-514">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26c59-514">Az.DataLakeStore</span></span>
- <span data-ttu-id="26c59-515">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="26c59-516">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="26c59-516">Az.Monitor</span></span>
- <span data-ttu-id="26c59-517">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-517">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="26c59-518">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="26c59-518">Az.KeyVault</span></span>
- <span data-ttu-id="26c59-519">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="26c59-519">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="26c59-520">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="26c59-520">Az.MachineLearning</span></span>
- <span data-ttu-id="26c59-521">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-521">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="26c59-522">Az.Media</span><span class="sxs-lookup"><span data-stu-id="26c59-522">Az.Media</span></span>
- <span data-ttu-id="26c59-523">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="26c59-523">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="26c59-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-524">Az.Network</span></span>
<span data-ttu-id="26c59-525">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="26c59-525">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="26c59-526">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="26c59-526">New cmdlets added:</span></span>
        - <span data-ttu-id="26c59-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26c59-527">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="26c59-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26c59-528">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="26c59-529">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26c59-529">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="26c59-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26c59-530">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="26c59-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26c59-531">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="26c59-532">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="26c59-532">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="26c59-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="26c59-533">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="26c59-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="26c59-534">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="26c59-535">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="26c59-535">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="26c59-536">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="26c59-536">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="26c59-537">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="26c59-537">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="26c59-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="26c59-538">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="26c59-539">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="26c59-539">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="26c59-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="26c59-540">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="26c59-541">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="26c59-541">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="26c59-542">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-542">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="26c59-543">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="26c59-543">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="26c59-544">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="26c59-544">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="26c59-545">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="26c59-545">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="26c59-546">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-546">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="26c59-547">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-547">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="26c59-548">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="26c59-548">Az.OperationalInsights</span></span>
- <span data-ttu-id="26c59-549">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="26c59-550">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="26c59-550">Az.Profile</span></span>
- <span data-ttu-id="26c59-551">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="26c59-551">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="26c59-552">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="26c59-552">Az.RecoveryServices</span></span>
- <span data-ttu-id="26c59-553">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-553">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="26c59-554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-554">Az.Resources</span></span>
- <span data-ttu-id="26c59-555">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="26c59-556">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="26c59-556">Az.ServiceFabric</span></span>
- <span data-ttu-id="26c59-557">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="26c59-557">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="26c59-558">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-558">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="26c59-559">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="26c59-559">Az.SIgnalR</span></span>
- <span data-ttu-id="26c59-560">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="26c59-560">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="26c59-561">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-561">Az.Sql</span></span>
- <span data-ttu-id="26c59-562">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="26c59-562">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="26c59-563">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="26c59-563">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="26c59-564">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-564">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="26c59-565">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="26c59-565">Az.Storage</span></span>
- <span data-ttu-id="26c59-566">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="26c59-567">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="26c59-567">Az.Websites</span></span>
- <span data-ttu-id="26c59-568">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="26c59-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="26c59-569">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="26c59-569">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="26c59-570">一般</span><span class="sxs-lookup"><span data-stu-id="26c59-570">General</span></span>

* <span data-ttu-id="26c59-571">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="26c59-571">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="26c59-572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-572">Az.Compute</span></span>

* <span data-ttu-id="26c59-573">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="26c59-573">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="26c59-574">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26c59-574">Az.DataLakeStore</span></span>

* <span data-ttu-id="26c59-575">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="26c59-575">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="26c59-576">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="26c59-576">Az.FrontDoor</span></span>

* <span data-ttu-id="26c59-577">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="26c59-577">Fixed some broken links</span></span>
    - <span data-ttu-id="26c59-578">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="26c59-578">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="26c59-579">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="26c59-579">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="26c59-580">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="26c59-580">Az.RecoveryServices</span></span>

* <span data-ttu-id="26c59-581">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="26c59-581">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="26c59-582">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="26c59-582">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="26c59-583">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-583">Az.Resources</span></span>

* <span data-ttu-id="26c59-584">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="26c59-584">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="26c59-585">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="26c59-585">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="26c59-586">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-586">Az.Sql</span></span>

* <span data-ttu-id="26c59-587">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="26c59-587">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="26c59-588">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-588">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="26c59-589">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="26c59-589">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="26c59-590">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="26c59-590">Az.Storage</span></span>

* <span data-ttu-id="26c59-591">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="26c59-591">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="26c59-592">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="26c59-592">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="26c59-593">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="26c59-593">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="26c59-594">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="26c59-594">Support Static Website configuration</span></span>
    - <span data-ttu-id="26c59-595">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="26c59-595">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="26c59-596">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="26c59-596">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="26c59-597">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="26c59-597">Az.Websites</span></span>

* <span data-ttu-id="26c59-598">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="26c59-598">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="26c59-599">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="26c59-599">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="26c59-600">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="26c59-600">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="26c59-601">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="26c59-601">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="26c59-602">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="26c59-602">Az.ApiManagement</span></span>
* <span data-ttu-id="26c59-603">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="26c59-603">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="26c59-604">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="26c59-604">Az.Automation</span></span>
* <span data-ttu-id="26c59-605">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-605">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="26c59-606">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-606">Added Update Management cmdlets</span></span>
* <span data-ttu-id="26c59-607">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-607">Added Source Control cmdlets</span></span>
* <span data-ttu-id="26c59-608">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-608">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="26c59-609">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="26c59-609">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="26c59-610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-610">Az.Compute</span></span>
* <span data-ttu-id="26c59-611">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="26c59-611">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="26c59-612">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="26c59-612">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="26c59-613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="26c59-613">Az.ContainerInstance</span></span>
* <span data-ttu-id="26c59-614">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="26c59-614">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="26c59-615">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="26c59-615">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="26c59-616">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="26c59-616">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="26c59-617">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-617">Az.Network</span></span>
* <span data-ttu-id="26c59-618">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="26c59-618">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="26c59-619">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="26c59-619">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="26c59-620">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="26c59-620">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="26c59-621">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="26c59-621">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="26c59-622">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="26c59-622">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="26c59-623">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="26c59-623">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="26c59-624">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="26c59-624">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="26c59-625">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="26c59-625">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="26c59-626">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="26c59-626">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="26c59-627">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="26c59-627">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="26c59-628">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="26c59-628">Az.Relay</span></span>
* <span data-ttu-id="26c59-629">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="26c59-629">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="26c59-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-630">Az.Resources</span></span>
* <span data-ttu-id="26c59-631">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="26c59-631">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="26c59-632">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="26c59-632">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="26c59-633">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="26c59-633">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="26c59-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="26c59-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="26c59-635">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="26c59-635">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="26c59-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-636">Az.Sql</span></span>
* <span data-ttu-id="26c59-637">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-637">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="26c59-638">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="26c59-638">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="26c59-639">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="26c59-639">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="26c59-640">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="26c59-640">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="26c59-641">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="26c59-641">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="26c59-642">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="26c59-642">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="26c59-643">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="26c59-643">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="26c59-644">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="26c59-644">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="26c59-645">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="26c59-645">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="26c59-646">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="26c59-646">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="26c59-647">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="26c59-647">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="26c59-648">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="26c59-648">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="26c59-649">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="26c59-649">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="26c59-650">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="26c59-650">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="26c59-651">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="26c59-651">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="26c59-652">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="26c59-652">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="26c59-653">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-653">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="26c59-654">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="26c59-654">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="26c59-655">一般</span><span class="sxs-lookup"><span data-stu-id="26c59-655">General</span></span>
* <span data-ttu-id="26c59-656">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="26c59-656">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="26c59-657">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="26c59-657">Az.Profile</span></span>
* <span data-ttu-id="26c59-658">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="26c59-658">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="26c59-659">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="26c59-659">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="26c59-660">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="26c59-660">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="26c59-661">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="26c59-661">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="26c59-662">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-662">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="26c59-663">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-663">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="26c59-664">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-664">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="26c59-665">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="26c59-665">Az.CognitiveServices</span></span>
* <span data-ttu-id="26c59-666">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="26c59-666">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-667">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-667">Az.Compute</span></span>
* <span data-ttu-id="26c59-668">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-668">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="26c59-669">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="26c59-669">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="26c59-670">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="26c59-670">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="26c59-671">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26c59-671">Az.DataLakeStore</span></span>
* <span data-ttu-id="26c59-672">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="26c59-672">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="26c59-673">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="26c59-673">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="26c59-674">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="26c59-674">Az.Insights</span></span>
* <span data-ttu-id="26c59-675">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="26c59-675">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="26c59-676">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="26c59-676">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="26c59-677">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="26c59-677">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="26c59-678">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="26c59-678">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="26c59-679">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-679">Az.Network</span></span>
* <span data-ttu-id="26c59-680">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="26c59-680">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="26c59-681">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="26c59-681">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="26c59-682">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="26c59-682">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="26c59-683">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="26c59-683">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="26c59-684">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="26c59-684">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="26c59-685">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="26c59-685">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="26c59-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="26c59-686">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="26c59-687">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="26c59-687">Az.PolicyInsights</span></span>
* <span data-ttu-id="26c59-688">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-688">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-689">Az.Resources</span></span>
* <span data-ttu-id="26c59-690">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="26c59-690">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="26c59-691">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="26c59-691">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="26c59-692">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="26c59-692">Az.ServiceBus</span></span>
* <span data-ttu-id="26c59-693">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="26c59-693">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="26c59-694">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="26c59-694">Az.ServiceFabric</span></span>
* <span data-ttu-id="26c59-695">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="26c59-695">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="26c59-696">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="26c59-696">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="26c59-697">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="26c59-697">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="26c59-698">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="26c59-698">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="26c59-699">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="26c59-699">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="26c59-700">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="26c59-700">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="26c59-701">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="26c59-701">Az.Profile</span></span>
* <span data-ttu-id="26c59-702">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-702">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="26c59-703">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="26c59-703">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-704">Az.Compute</span></span>
* <span data-ttu-id="26c59-705">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="26c59-705">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="26c59-706">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26c59-706">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="26c59-707">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="26c59-707">Az.DataLakeStore</span></span>
* <span data-ttu-id="26c59-708">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="26c59-708">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="26c59-709">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="26c59-709">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="26c59-710">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="26c59-710">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="26c59-711">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="26c59-711">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="26c59-712">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="26c59-712">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="26c59-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-713">Az.Network</span></span>
* <span data-ttu-id="26c59-714">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="26c59-714">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="26c59-715">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26c59-715">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-716">Az.Resources</span></span>
* <span data-ttu-id="26c59-717">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="26c59-717">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="26c59-718">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="26c59-718">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="26c59-719">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="26c59-719">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="26c59-720">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="26c59-720">Azure.Storage</span></span>
* <span data-ttu-id="26c59-721">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-721">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="26c59-722">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="26c59-722">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="26c59-723">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="26c59-723">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="26c59-724">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="26c59-724">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="26c59-725">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="26c59-725">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="26c59-726">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="26c59-726">Az.CognitiveServices</span></span>
* <span data-ttu-id="26c59-727">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="26c59-727">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="26c59-728">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="26c59-728">Az.Compute</span></span>
* <span data-ttu-id="26c59-729">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="26c59-729">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="26c59-730">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="26c59-730">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="26c59-731">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="26c59-731">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="26c59-732">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="26c59-732">Az.DataFactoryV2</span></span>
* <span data-ttu-id="26c59-733">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="26c59-733">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="26c59-734">Az.Network</span><span class="sxs-lookup"><span data-stu-id="26c59-734">Az.Network</span></span>
* <span data-ttu-id="26c59-735">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="26c59-735">Added NetworkProfile functionality.</span></span> <span data-ttu-id="26c59-736">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-736">new cmdlets added</span></span>
    - <span data-ttu-id="26c59-737">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="26c59-737">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="26c59-738">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="26c59-738">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="26c59-739">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="26c59-739">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="26c59-740">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="26c59-740">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="26c59-741">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="26c59-741">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="26c59-742">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="26c59-742">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="26c59-743">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="26c59-743">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="26c59-744">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-744">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="26c59-745">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="26c59-745">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="26c59-746">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="26c59-746">Az.RedisCache</span></span>
* <span data-ttu-id="26c59-747">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="26c59-747">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="26c59-748">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="26c59-748">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="26c59-749">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="26c59-749">Az.Resources</span></span>
* <span data-ttu-id="26c59-750">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="26c59-750">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="26c59-751">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="26c59-751">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="26c59-752">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="26c59-752">Az.Sql</span></span>
* <span data-ttu-id="26c59-753">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="26c59-753">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="26c59-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="26c59-754">Az.Websites</span></span>
* <span data-ttu-id="26c59-755">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="26c59-755">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="26c59-756">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="26c59-756">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="26c59-757">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="26c59-757">0.2.0 - September 2018</span></span>
 <span data-ttu-id="26c59-758">初始版本</span><span class="sxs-lookup"><span data-stu-id="26c59-758">Initial Release</span></span>