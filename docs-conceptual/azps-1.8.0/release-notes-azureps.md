---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 8a9a399f72ed9e3e9a3cbc09c8a4abaa91339c24
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "71319298"
---
## <a name="180---april-2019"></a><span data-ttu-id="b7679-103">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="b7679-103">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b7679-104">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b7679-104">Highlights since the last major release</span></span>
* <span data-ttu-id="b7679-105">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="b7679-105">General availability of `Az` module</span></span>
* <span data-ttu-id="b7679-106">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b7679-106">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b7679-107">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b7679-107">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b7679-108">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b7679-108">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b7679-109">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="b7679-109">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b7679-110">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="b7679-110">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b7679-111">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-111">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b7679-112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-112">Az.Accounts</span></span>
* <span data-ttu-id="b7679-113">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="b7679-113">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="b7679-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b7679-114">Az.Batch</span></span>
* <span data-ttu-id="b7679-115">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-115">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b7679-116">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b7679-116">Az.Cdn</span></span>
* <span data-ttu-id="b7679-117">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-117">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b7679-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7679-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="b7679-119">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-119">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-120">Az.Compute</span></span>
* <span data-ttu-id="b7679-121">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="b7679-121">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="b7679-122">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-122">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b7679-123">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b7679-123">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b7679-124">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b7679-124">Az.DataFactory</span></span>
* <span data-ttu-id="b7679-125">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="b7679-125">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7679-126">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7679-126">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7679-127">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-127">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b7679-128">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b7679-128">Az.EventGrid</span></span>
* <span data-ttu-id="b7679-129">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7679-129">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b7679-130">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7679-130">Az.EventHub</span></span>
* <span data-ttu-id="b7679-131">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-131">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="b7679-132">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b7679-132">Az.HDInsight</span></span>
* <span data-ttu-id="b7679-133">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-133">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b7679-134">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b7679-134">Az.IotHub</span></span>
* <span data-ttu-id="b7679-135">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b7679-136">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7679-136">Az.KeyVault</span></span>
* <span data-ttu-id="b7679-137">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-137">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b7679-138">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b7679-138">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="b7679-139">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b7679-139">Az.MachineLearning</span></span>
* <span data-ttu-id="b7679-140">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="b7679-141">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b7679-141">Az.Media</span></span>
* <span data-ttu-id="b7679-142">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-142">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b7679-143">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b7679-143">Az.Monitor</span></span>
  * <span data-ttu-id="b7679-144">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-144">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="b7679-145">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b7679-145">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="b7679-146">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b7679-146">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="b7679-147">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b7679-147">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b7679-148">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b7679-148">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="b7679-149">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="b7679-149">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="b7679-150">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="b7679-150">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7679-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-151">Az.Network</span></span>
* <span data-ttu-id="b7679-152">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b7679-153">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b7679-153">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="b7679-154">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b7679-154">Az.NotificationHubs</span></span>
* <span data-ttu-id="b7679-155">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-155">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b7679-156">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b7679-156">Az.OperationalInsights</span></span>
* <span data-ttu-id="b7679-157">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-157">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="b7679-158">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b7679-158">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="b7679-159">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b7679-160">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7679-160">Az.RecoveryServices</span></span>
* <span data-ttu-id="b7679-161">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-161">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b7679-162">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="b7679-162">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="b7679-163">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="b7679-163">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="b7679-164">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="b7679-164">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b7679-165">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b7679-165">Az.RedisCache</span></span>
* <span data-ttu-id="b7679-166">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-166">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-167">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-167">Az.Resources</span></span>
* <span data-ttu-id="b7679-168">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b7679-168">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-169">Az.Sql</span></span>
* <span data-ttu-id="b7679-170">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="b7679-170">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="b7679-171">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-171">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b7679-172">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="b7679-172">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="b7679-173">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="b7679-173">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="b7679-174">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="b7679-174">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="b7679-175">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="b7679-175">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="b7679-176">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="b7679-176">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7679-177">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7679-177">Az.Websites</span></span>
* <span data-ttu-id="b7679-178">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="b7679-178">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="b7679-179">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="b7679-180">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="b7679-180">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="b7679-181">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="b7679-181">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="b7679-182">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="b7679-182">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b7679-183">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b7679-183">Highlights since the last major release</span></span>
* <span data-ttu-id="b7679-184">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="b7679-184">General availability of `Az` module</span></span>
* <span data-ttu-id="b7679-185">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b7679-185">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b7679-186">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b7679-186">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b7679-187">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b7679-187">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b7679-188">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="b7679-188">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b7679-189">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="b7679-189">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b7679-190">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-190">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="b7679-191">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-191">Az.Accounts</span></span>
* <span data-ttu-id="b7679-192">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="b7679-192">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b7679-193">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7679-193">Az.AnalysisServices</span></span>
* <span data-ttu-id="b7679-194">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="b7679-194">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="b7679-195">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="b7679-195">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b7679-196">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7679-196">Az.Automation</span></span>
* <span data-ttu-id="b7679-197">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="b7679-197">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="b7679-198">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="b7679-198">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="b7679-199">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="b7679-199">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-200">Az.Compute</span></span>
* <span data-ttu-id="b7679-201">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b7679-201">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="b7679-202">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="b7679-202">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="b7679-203">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b7679-203">Az.ContainerInstance</span></span>
* <span data-ttu-id="b7679-204">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="b7679-204">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b7679-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b7679-205">Az.DataFactory</span></span>
* <span data-ttu-id="b7679-206">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="b7679-206">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="b7679-207">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7679-207">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-208">Az.Resources</span></span>
* <span data-ttu-id="b7679-209">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="b7679-209">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="b7679-210">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="b7679-210">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="b7679-211">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="b7679-211">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="b7679-212">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b7679-212">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="b7679-213">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="b7679-213">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="b7679-214">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="b7679-214">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-215">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-215">Az.Sql</span></span>
* <span data-ttu-id="b7679-216">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="b7679-216">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b7679-217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7679-217">Az.Storage</span></span>
* <span data-ttu-id="b7679-218">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="b7679-218">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="b7679-219">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7679-219">New-AzStorageContext</span></span>
* <span data-ttu-id="b7679-220">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="b7679-220">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="b7679-221">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b7679-221">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b7679-222">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b7679-222">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="b7679-223">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7679-223">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="b7679-224">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7679-224">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="b7679-225">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-225">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="b7679-226">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b7679-226">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b7679-227">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b7679-227">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="b7679-228">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b7679-228">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="b7679-229">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b7679-229">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="b7679-230">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="b7679-230">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="b7679-231">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="b7679-231">Highlights since the last major release</span></span>
* <span data-ttu-id="b7679-232">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="b7679-232">General availability of `Az` module</span></span>
* <span data-ttu-id="b7679-233">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="b7679-233">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="b7679-234">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="b7679-234">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="b7679-235">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b7679-235">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="b7679-236">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="b7679-236">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b7679-237">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="b7679-237">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="b7679-238">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-238">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b7679-239">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7679-239">Az.Automation</span></span>
* <span data-ttu-id="b7679-240">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="b7679-240">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="b7679-241">動態分組</span><span class="sxs-lookup"><span data-stu-id="b7679-241">Dynamic grouping</span></span>
    * <span data-ttu-id="b7679-242">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="b7679-242">Pre-Post script</span></span>
    * <span data-ttu-id="b7679-243">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="b7679-243">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-244">Az.Compute</span></span>
* <span data-ttu-id="b7679-245">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-245">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="b7679-246">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="b7679-246">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b7679-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7679-247">Az.KeyVault</span></span>
* <span data-ttu-id="b7679-248">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b7679-248">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7679-249">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-249">Az.Network</span></span>
* <span data-ttu-id="b7679-250">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="b7679-250">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="b7679-251">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="b7679-251">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b7679-252">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7679-252">Az.RecoveryServices</span></span>
* <span data-ttu-id="b7679-253">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="b7679-253">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="b7679-254">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="b7679-254">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-255">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-255">Az.Resources</span></span>
* <span data-ttu-id="b7679-256">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b7679-256">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="b7679-257">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="b7679-257">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-258">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-258">Az.Sql</span></span>
* <span data-ttu-id="b7679-259">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="b7679-259">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b7679-260">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7679-260">Az.Storage</span></span>
* <span data-ttu-id="b7679-261">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="b7679-261">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="b7679-262">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b7679-262">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b7679-263">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b7679-263">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b7679-264">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="b7679-264">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="b7679-265">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b7679-265">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="b7679-266">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b7679-266">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="b7679-267">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b7679-267">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7679-268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7679-268">Az.Websites</span></span>
* <span data-ttu-id="b7679-269">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="b7679-269">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="b7679-270">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="b7679-270">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7679-271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-271">Az.Accounts</span></span>
* <span data-ttu-id="b7679-272">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-272">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="b7679-273">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="b7679-273">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b7679-274">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7679-274">Az.Automation</span></span>
* <span data-ttu-id="b7679-275">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-275">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="b7679-276">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="b7679-276">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="b7679-277">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="b7679-277">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b7679-278">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b7679-278">Az.Cdn</span></span>
* <span data-ttu-id="b7679-279">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-279">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-280">Az.Compute</span></span>
* <span data-ttu-id="b7679-281">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b7679-281">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b7679-282">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b7679-282">Az.DataFactory</span></span>
* <span data-ttu-id="b7679-283">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="b7679-283">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b7679-284">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b7679-284">Az.LogicApp</span></span>
* <span data-ttu-id="b7679-285">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="b7679-285">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7679-286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-286">Az.Network</span></span>
* <span data-ttu-id="b7679-287">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="b7679-287">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b7679-288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7679-288">Az.RecoveryServices</span></span>
* <span data-ttu-id="b7679-289">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="b7679-289">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="b7679-290">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="b7679-290">SDK Update</span></span>
* <span data-ttu-id="b7679-291">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="b7679-291">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="b7679-292">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="b7679-292">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-293">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-293">Az.Resources</span></span>
* <span data-ttu-id="b7679-294">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-294">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="b7679-295">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="b7679-295">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="b7679-296">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-296">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="b7679-297">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="b7679-297">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="b7679-298">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-298">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="b7679-299">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="b7679-299">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-300">Az.Sql</span></span>
* <span data-ttu-id="b7679-301">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="b7679-301">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="b7679-302">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="b7679-302">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b7679-303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7679-303">Az.Storage</span></span>
* <span data-ttu-id="b7679-304">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b7679-304">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="b7679-305">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="b7679-305">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="b7679-306">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7679-306">Az.AnalysisServices</span></span>
* <span data-ttu-id="b7679-307">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-307">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b7679-308">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7679-308">Az.Automation</span></span>
* <span data-ttu-id="b7679-309">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="b7679-309">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="b7679-310">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-310">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="b7679-311">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="b7679-311">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="b7679-312">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7679-312">Az.CognitiveServices</span></span>
* <span data-ttu-id="b7679-313">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="b7679-313">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-314">Az.Compute</span></span>
* <span data-ttu-id="b7679-315">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="b7679-315">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="b7679-316">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="b7679-316">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="b7679-317">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-317">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="b7679-318">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="b7679-318">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7679-319">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7679-319">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7679-320">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-320">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="b7679-321">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="b7679-321">Az.EventHub</span></span>
* <span data-ttu-id="b7679-322">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="b7679-322">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="b7679-323">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7679-323">Az.KeyVault</span></span>
* <span data-ttu-id="b7679-324">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="b7679-324">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b7679-325">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b7679-325">Az.LogicApp</span></span>
* <span data-ttu-id="b7679-326">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="b7679-326">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="b7679-327">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="b7679-327">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="b7679-328">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-328">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="b7679-329">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b7679-329">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b7679-330">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b7679-330">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b7679-331">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b7679-331">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="b7679-332">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b7679-332">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="b7679-333">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-333">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="b7679-334">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7679-334">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b7679-335">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7679-335">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b7679-336">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7679-336">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="b7679-337">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7679-337">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="b7679-338">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="b7679-338">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="b7679-339">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b7679-339">Az.Monitor</span></span>
* <span data-ttu-id="b7679-340">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="b7679-340">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7679-341">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-341">Az.Network</span></span>
* <span data-ttu-id="b7679-342">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="b7679-342">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="b7679-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b7679-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="b7679-344">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="b7679-344">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="b7679-345">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="b7679-345">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="b7679-346">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="b7679-346">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="b7679-347">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-347">Az.Resources</span></span>
* <span data-ttu-id="b7679-348">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-348">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b7679-349">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="b7679-350">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-350">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="b7679-351">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="b7679-351">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-352">Az.Sql</span></span>
* <span data-ttu-id="b7679-353">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="b7679-353">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="b7679-354">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="b7679-354">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7679-355">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7679-355">Az.Websites</span></span>
* <span data-ttu-id="b7679-356">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="b7679-356">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="b7679-357">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="b7679-357">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7679-358">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-358">Az.Accounts</span></span>
* <span data-ttu-id="b7679-359">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b7679-359">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b7679-360">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7679-360">Az.AnalysisServices</span></span>
<span data-ttu-id="b7679-361">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="b7679-361">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-362">Az.Compute</span></span>
* <span data-ttu-id="b7679-363">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="b7679-363">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="b7679-364">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="b7679-364">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="b7679-365">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="b7679-365">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b7679-366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7679-366">Az.RecoveryServices</span></span>
<span data-ttu-id="b7679-367">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="b7679-367">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-368">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-368">Az.Resources</span></span>
* <span data-ttu-id="b7679-369">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="b7679-369">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="b7679-370">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="b7679-370">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="b7679-371">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-371">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="b7679-372">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="b7679-372">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-373">Az.Sql</span></span>
* <span data-ttu-id="b7679-374">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7679-374">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="b7679-375">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-375">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="b7679-376">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="b7679-376">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="b7679-377">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="b7679-377">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7679-378">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-378">Az.Accounts</span></span>
* <span data-ttu-id="b7679-379">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="b7679-379">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="b7679-380">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b7679-380">Az.AnalysisServices</span></span>
* <span data-ttu-id="b7679-381">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="b7679-381">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="b7679-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7679-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="b7679-383">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="b7679-383">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="b7679-384">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="b7679-384">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7679-385">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-385">Az.Accounts</span></span>
* <span data-ttu-id="b7679-386">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="b7679-386">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="b7679-387">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-387">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b7679-388">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="b7679-388">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="b7679-389">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="b7679-389">Az.Aks</span></span>
* <span data-ttu-id="b7679-390">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-390">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="b7679-391">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7679-391">Az.Automation</span></span>
* <span data-ttu-id="b7679-392">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="b7679-392">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="b7679-393">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-393">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="b7679-394">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="b7679-394">Az.Cdn</span></span>
* <span data-ttu-id="b7679-395">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-395">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-396">Az.Compute</span></span>
* <span data-ttu-id="b7679-397">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-397">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="b7679-398">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7679-398">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="b7679-399">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="b7679-399">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="b7679-400">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b7679-400">Az.ContainerRegistry</span></span>
* <span data-ttu-id="b7679-401">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-401">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="b7679-402">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="b7679-402">Az.DataFactory</span></span>
* <span data-ttu-id="b7679-403">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="b7679-403">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7679-404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7679-404">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7679-405">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-405">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="b7679-406">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="b7679-406">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="b7679-407">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-407">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b7679-408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b7679-408">Az.IotHub</span></span>
* <span data-ttu-id="b7679-409">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7679-409">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="b7679-410">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7679-410">Az.KeyVault</span></span>
* <span data-ttu-id="b7679-411">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-411">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7679-412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-412">Az.Network</span></span>
* <span data-ttu-id="b7679-413">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-413">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-414">Az.Resources</span></span>
* <span data-ttu-id="b7679-415">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="b7679-415">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="b7679-416">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-416">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="b7679-417">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="b7679-417">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="b7679-418">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-418">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="b7679-419">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="b7679-420">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-420">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="b7679-421">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="b7679-421">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b7679-422">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7679-422">Az.ServiceFabric</span></span>
* <span data-ttu-id="b7679-423">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="b7679-423">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="b7679-424">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b7679-424">Fix some error messages.</span></span>
* <span data-ttu-id="b7679-425">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="b7679-425">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="b7679-426">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="b7679-426">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b7679-427">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b7679-427">Az.SignalR</span></span>
* <span data-ttu-id="b7679-428">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-428">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-429">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-429">Az.Sql</span></span>
* <span data-ttu-id="b7679-430">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-430">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b7679-431">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="b7679-431">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="b7679-432">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-432">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="b7679-433">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="b7679-433">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b7679-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7679-434">Az.Storage</span></span>
* <span data-ttu-id="b7679-435">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-435">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b7679-436">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="b7679-436">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="b7679-437">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b7679-437">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="b7679-438">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="b7679-438">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="b7679-439">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b7679-439">Az.TrafficManager</span></span>
* <span data-ttu-id="b7679-440">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-440">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7679-441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7679-441">Az.Websites</span></span>
* <span data-ttu-id="b7679-442">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="b7679-442">Update incorrect online help URLs</span></span>
* <span data-ttu-id="b7679-443">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="b7679-443">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="b7679-444">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="b7679-444">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="b7679-445">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="b7679-445">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="b7679-446">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-446">Az.Accounts</span></span>
* <span data-ttu-id="b7679-447">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="b7679-447">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-448">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-448">Az.Compute</span></span>
* <span data-ttu-id="b7679-449">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="b7679-449">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="b7679-450">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="b7679-450">Updated the description of ID in help files</span></span>
* <span data-ttu-id="b7679-451">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="b7679-451">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7679-452">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7679-452">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7679-453">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="b7679-453">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="b7679-454">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="b7679-454">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="b7679-455">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b7679-455">Az.EventGrid</span></span>
* <span data-ttu-id="b7679-456">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b7679-456">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="b7679-457">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="b7679-457">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="b7679-458">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="b7679-458">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b7679-459">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="b7679-459">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b7679-460">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="b7679-460">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b7679-461">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="b7679-461">Dead letter endpoint.</span></span>
    - <span data-ttu-id="b7679-462">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="b7679-462">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="b7679-463">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="b7679-463">Event Time-To-Live,</span></span>
        - <span data-ttu-id="b7679-464">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="b7679-464">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="b7679-465">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="b7679-465">Dead letter endpoint.</span></span>
* <span data-ttu-id="b7679-466">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="b7679-466">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="b7679-467">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="b7679-467">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="b7679-468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="b7679-468">Az.IotHub</span></span>
* <span data-ttu-id="b7679-469">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="b7679-469">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="b7679-470">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b7679-470">Az.LogicApp</span></span>
* <span data-ttu-id="b7679-471">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="b7679-471">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-472">Az.Resources</span></span>
* <span data-ttu-id="b7679-473">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="b7679-473">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="b7679-474">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="b7679-474">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="b7679-475">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="b7679-475">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b7679-476">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="b7679-476">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="b7679-477">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="b7679-477">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="b7679-478">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="b7679-478">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="b7679-479">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="b7679-479">Az.SignalR</span></span>
* <span data-ttu-id="b7679-480">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="b7679-480">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-481">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-481">Az.Sql</span></span>
* <span data-ttu-id="b7679-482">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="b7679-482">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="b7679-483">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7679-483">Az.Storage</span></span>
* <span data-ttu-id="b7679-484">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="b7679-484">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="b7679-485">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7679-485">New-AzStorageContext</span></span>
* <span data-ttu-id="b7679-486">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="b7679-486">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="b7679-487">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b7679-487">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7679-488">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7679-488">Az.Websites</span></span>
* <span data-ttu-id="b7679-489">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="b7679-489">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="b7679-490">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="b7679-490">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="b7679-491">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="b7679-491">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="b7679-492">一般</span><span class="sxs-lookup"><span data-stu-id="b7679-492">General</span></span>

- <span data-ttu-id="b7679-493">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="b7679-493">General Availability of Az Module</span></span>
- <span data-ttu-id="b7679-494">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="b7679-494">Online help for each module</span></span>
- <span data-ttu-id="b7679-495">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="b7679-495">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="b7679-496">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-496">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="b7679-497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-497">Az.Accounts</span></span>
- <span data-ttu-id="b7679-498">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="b7679-498">Changed from Az.Profile</span></span>
- <span data-ttu-id="b7679-499">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="b7679-499">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b7679-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7679-500">Az.ApiManagement</span></span>
- <span data-ttu-id="b7679-501">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="b7679-501">Fixes for #7002</span></span>
- <span data-ttu-id="b7679-502">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-502">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="b7679-503">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="b7679-503">Az.Batch</span></span>
- <span data-ttu-id="b7679-504">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="b7679-504">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="b7679-505">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="b7679-505">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="b7679-506">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-506">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="b7679-507">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="b7679-507">Az.Billing</span></span>
- <span data-ttu-id="b7679-508">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-508">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="b7679-509">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="b7679-509">Az.CognitivServices</span></span>
- <span data-ttu-id="b7679-510">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="b7679-510">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="b7679-511">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="b7679-511">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b7679-512">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b7679-512">Az.ContainerInstance</span></span>
- <span data-ttu-id="b7679-513">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="b7679-513">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="b7679-514">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b7679-514">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="b7679-515">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-515">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b7679-516">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7679-516">Az.DataLakeStore</span></span>
- <span data-ttu-id="b7679-517">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-517">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="b7679-518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="b7679-518">Az.Monitor</span></span>
- <span data-ttu-id="b7679-519">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-519">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="b7679-520">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b7679-520">Az.KeyVault</span></span>
- <span data-ttu-id="b7679-521">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="b7679-521">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="b7679-522">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b7679-522">Az.MachineLearning</span></span>
- <span data-ttu-id="b7679-523">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-523">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="b7679-524">Az.Media</span><span class="sxs-lookup"><span data-stu-id="b7679-524">Az.Media</span></span>
- <span data-ttu-id="b7679-525">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="b7679-525">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b7679-526">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-526">Az.Network</span></span>
<span data-ttu-id="b7679-527">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="b7679-527">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="b7679-528">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="b7679-528">New cmdlets added:</span></span>
        - <span data-ttu-id="b7679-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7679-529">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7679-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7679-530">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7679-531">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7679-531">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7679-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7679-532">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7679-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7679-533">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="b7679-534">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b7679-534">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="b7679-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b7679-535">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="b7679-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7679-536">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="b7679-537">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7679-537">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="b7679-538">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7679-538">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="b7679-539">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7679-539">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b7679-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7679-540">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="b7679-541">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7679-541">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="b7679-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b7679-542">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="b7679-543">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="b7679-543">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="b7679-544">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-544">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="b7679-545">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b7679-545">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b7679-546">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b7679-546">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="b7679-547">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b7679-547">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="b7679-548">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-548">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="b7679-549">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-549">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="b7679-550">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b7679-550">Az.OperationalInsights</span></span>
- <span data-ttu-id="b7679-551">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-551">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="b7679-552">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b7679-552">Az.Profile</span></span>
- <span data-ttu-id="b7679-553">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="b7679-553">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b7679-554">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7679-554">Az.RecoveryServices</span></span>
- <span data-ttu-id="b7679-555">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-555">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="b7679-556">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-556">Az.Resources</span></span>
- <span data-ttu-id="b7679-557">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-557">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b7679-558">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7679-558">Az.ServiceFabric</span></span>
- <span data-ttu-id="b7679-559">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="b7679-559">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="b7679-560">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-560">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="b7679-561">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="b7679-561">Az.SIgnalR</span></span>
- <span data-ttu-id="b7679-562">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="b7679-562">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="b7679-563">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-563">Az.Sql</span></span>
- <span data-ttu-id="b7679-564">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="b7679-564">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="b7679-565">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="b7679-565">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="b7679-566">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-566">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="b7679-567">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7679-567">Az.Storage</span></span>
- <span data-ttu-id="b7679-568">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-568">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b7679-569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7679-569">Az.Websites</span></span>
- <span data-ttu-id="b7679-570">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="b7679-570">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="b7679-571">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="b7679-571">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="b7679-572">一般</span><span class="sxs-lookup"><span data-stu-id="b7679-572">General</span></span>

* <span data-ttu-id="b7679-573">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="b7679-573">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="b7679-574">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-574">Az.Compute</span></span>

* <span data-ttu-id="b7679-575">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="b7679-575">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="b7679-576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7679-576">Az.DataLakeStore</span></span>

* <span data-ttu-id="b7679-577">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="b7679-577">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="b7679-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b7679-578">Az.FrontDoor</span></span>

* <span data-ttu-id="b7679-579">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="b7679-579">Fixed some broken links</span></span>
    - <span data-ttu-id="b7679-580">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="b7679-580">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="b7679-581">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="b7679-581">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="b7679-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b7679-582">Az.RecoveryServices</span></span>

* <span data-ttu-id="b7679-583">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="b7679-583">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="b7679-584">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="b7679-584">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="b7679-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-585">Az.Resources</span></span>

* <span data-ttu-id="b7679-586">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="b7679-586">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="b7679-587">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="b7679-587">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="b7679-588">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-588">Az.Sql</span></span>

* <span data-ttu-id="b7679-589">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="b7679-589">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="b7679-590">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-590">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="b7679-591">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="b7679-591">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="b7679-592">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="b7679-592">Az.Storage</span></span>

* <span data-ttu-id="b7679-593">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="b7679-593">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="b7679-594">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="b7679-594">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="b7679-595">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b7679-595">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b7679-596">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="b7679-596">Support Static Website configuration</span></span>
    - <span data-ttu-id="b7679-597">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b7679-597">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="b7679-598">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="b7679-598">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="b7679-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7679-599">Az.Websites</span></span>

* <span data-ttu-id="b7679-600">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b7679-600">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="b7679-601">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="b7679-601">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="b7679-602">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="b7679-602">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="b7679-603">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="b7679-603">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="b7679-604">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b7679-604">Az.ApiManagement</span></span>
* <span data-ttu-id="b7679-605">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="b7679-605">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="b7679-606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="b7679-606">Az.Automation</span></span>
* <span data-ttu-id="b7679-607">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-607">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="b7679-608">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-608">Added Update Management cmdlets</span></span>
* <span data-ttu-id="b7679-609">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-609">Added Source Control cmdlets</span></span>
* <span data-ttu-id="b7679-610">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-610">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="b7679-611">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="b7679-611">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="b7679-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-612">Az.Compute</span></span>
* <span data-ttu-id="b7679-613">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="b7679-613">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="b7679-614">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="b7679-614">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="b7679-615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b7679-615">Az.ContainerInstance</span></span>
* <span data-ttu-id="b7679-616">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="b7679-616">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="b7679-617">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b7679-617">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="b7679-618">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="b7679-618">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="b7679-619">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-619">Az.Network</span></span>
* <span data-ttu-id="b7679-620">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b7679-620">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="b7679-621">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="b7679-621">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="b7679-622">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="b7679-622">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="b7679-623">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="b7679-623">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="b7679-624">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b7679-624">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b7679-625">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="b7679-625">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="b7679-626">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="b7679-626">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="b7679-627">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b7679-627">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b7679-628">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="b7679-628">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="b7679-629">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="b7679-629">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="b7679-630">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="b7679-630">Az.Relay</span></span>
* <span data-ttu-id="b7679-631">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="b7679-631">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="b7679-632">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-632">Az.Resources</span></span>
* <span data-ttu-id="b7679-633">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="b7679-633">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="b7679-634">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="b7679-634">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="b7679-635">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="b7679-635">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="b7679-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7679-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="b7679-637">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="b7679-637">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="b7679-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-638">Az.Sql</span></span>
* <span data-ttu-id="b7679-639">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-639">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="b7679-640">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7679-640">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b7679-641">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7679-641">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b7679-642">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7679-642">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b7679-643">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7679-643">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="b7679-644">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7679-644">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b7679-645">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7679-645">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b7679-646">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7679-646">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="b7679-647">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7679-647">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="b7679-648">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="b7679-648">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="b7679-649">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="b7679-649">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="b7679-650">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="b7679-650">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="b7679-651">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="b7679-651">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b7679-652">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="b7679-652">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="b7679-653">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="b7679-653">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="b7679-654">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="b7679-654">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="b7679-655">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-655">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="b7679-656">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="b7679-656">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b7679-657">一般</span><span class="sxs-lookup"><span data-stu-id="b7679-657">General</span></span>
* <span data-ttu-id="b7679-658">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="b7679-658">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="b7679-659">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b7679-659">Az.Profile</span></span>
* <span data-ttu-id="b7679-660">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b7679-660">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="b7679-661">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="b7679-661">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="b7679-662">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="b7679-662">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="b7679-663">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="b7679-663">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="b7679-664">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-664">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="b7679-665">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-665">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="b7679-666">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-666">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="b7679-667">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7679-667">Az.CognitiveServices</span></span>
* <span data-ttu-id="b7679-668">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="b7679-668">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-669">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-669">Az.Compute</span></span>
* <span data-ttu-id="b7679-670">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-670">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="b7679-671">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="b7679-671">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="b7679-672">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="b7679-672">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7679-673">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7679-673">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7679-674">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="b7679-674">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="b7679-675">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="b7679-675">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="b7679-676">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="b7679-676">Az.Insights</span></span>
* <span data-ttu-id="b7679-677">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="b7679-677">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="b7679-678">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="b7679-678">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="b7679-679">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="b7679-679">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="b7679-680">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="b7679-680">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7679-681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-681">Az.Network</span></span>
* <span data-ttu-id="b7679-682">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="b7679-682">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="b7679-683">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b7679-683">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="b7679-684">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b7679-684">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="b7679-685">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b7679-685">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="b7679-686">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b7679-686">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b7679-687">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b7679-687">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b7679-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b7679-688">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="b7679-689">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b7679-689">Az.PolicyInsights</span></span>
* <span data-ttu-id="b7679-690">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-690">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-691">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-691">Az.Resources</span></span>
* <span data-ttu-id="b7679-692">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="b7679-692">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="b7679-693">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="b7679-693">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="b7679-694">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b7679-694">Az.ServiceBus</span></span>
* <span data-ttu-id="b7679-695">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="b7679-695">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="b7679-696">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b7679-696">Az.ServiceFabric</span></span>
* <span data-ttu-id="b7679-697">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="b7679-697">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="b7679-698">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="b7679-698">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="b7679-699">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="b7679-699">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="b7679-700">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="b7679-700">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="b7679-701">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="b7679-701">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="b7679-702">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="b7679-702">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="b7679-703">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="b7679-703">Az.Profile</span></span>
* <span data-ttu-id="b7679-704">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-704">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="b7679-705">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="b7679-705">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-706">Az.Compute</span></span>
* <span data-ttu-id="b7679-707">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="b7679-707">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="b7679-708">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7679-708">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="b7679-709">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b7679-709">Az.DataLakeStore</span></span>
* <span data-ttu-id="b7679-710">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="b7679-710">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="b7679-711">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b7679-711">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="b7679-712">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="b7679-712">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b7679-713">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b7679-713">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="b7679-714">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b7679-714">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7679-715">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-715">Az.Network</span></span>
* <span data-ttu-id="b7679-716">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="b7679-716">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="b7679-717">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7679-717">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-718">Az.Resources</span></span>
* <span data-ttu-id="b7679-719">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="b7679-719">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="b7679-720">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="b7679-720">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="b7679-721">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="b7679-721">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="b7679-722">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b7679-722">Azure.Storage</span></span>
* <span data-ttu-id="b7679-723">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-723">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="b7679-724">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b7679-724">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="b7679-725">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b7679-725">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="b7679-726">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="b7679-726">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="b7679-727">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="b7679-727">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="b7679-728">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b7679-728">Az.CognitiveServices</span></span>
* <span data-ttu-id="b7679-729">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="b7679-729">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="b7679-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="b7679-730">Az.Compute</span></span>
* <span data-ttu-id="b7679-731">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="b7679-731">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="b7679-732">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="b7679-732">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="b7679-733">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="b7679-733">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="b7679-734">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b7679-734">Az.DataFactoryV2</span></span>
* <span data-ttu-id="b7679-735">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="b7679-735">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="b7679-736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="b7679-736">Az.Network</span></span>
* <span data-ttu-id="b7679-737">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="b7679-737">Added NetworkProfile functionality.</span></span> <span data-ttu-id="b7679-738">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-738">new cmdlets added</span></span>
    - <span data-ttu-id="b7679-739">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7679-739">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="b7679-740">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7679-740">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="b7679-741">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7679-741">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="b7679-742">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="b7679-742">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="b7679-743">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="b7679-743">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="b7679-744">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="b7679-744">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="b7679-745">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="b7679-745">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="b7679-746">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-746">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="b7679-747">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b7679-747">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="b7679-748">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b7679-748">Az.RedisCache</span></span>
* <span data-ttu-id="b7679-749">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="b7679-749">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="b7679-750">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="b7679-750">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="b7679-751">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="b7679-751">Az.Resources</span></span>
* <span data-ttu-id="b7679-752">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b7679-752">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="b7679-753">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="b7679-753">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="b7679-754">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="b7679-754">Az.Sql</span></span>
* <span data-ttu-id="b7679-755">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="b7679-755">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="b7679-756">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="b7679-756">Az.Websites</span></span>
* <span data-ttu-id="b7679-757">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="b7679-757">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="b7679-758">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="b7679-758">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="b7679-759">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="b7679-759">0.2.0 - September 2018</span></span>
 <span data-ttu-id="b7679-760">初始版本</span><span class="sxs-lookup"><span data-stu-id="b7679-760">Initial Release</span></span>