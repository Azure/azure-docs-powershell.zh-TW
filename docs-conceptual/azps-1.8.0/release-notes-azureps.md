---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/30/2019
ms.openlocfilehash: 34b21292ccc47bb53b6609cd637ef18338a45cd3
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/28/2020
ms.locfileid: "84121465"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="e57a3-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="e57a3-103">Azure PowerShell release notes</span></span>
## <a name="180---april-2019"></a><span data-ttu-id="e57a3-104">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-104">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e57a3-105">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e57a3-105">Highlights since the last major release</span></span>
* <span data-ttu-id="e57a3-106">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="e57a3-106">General availability of `Az` module</span></span>
* <span data-ttu-id="e57a3-107">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e57a3-107">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e57a3-108">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e57a3-108">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e57a3-109">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-109">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e57a3-110">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="e57a3-110">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e57a3-111">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-111">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e57a3-112">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-112">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e57a3-113">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-113">Az.Accounts</span></span>
* <span data-ttu-id="e57a3-114">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="e57a3-114">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e57a3-115">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e57a3-115">Az.Batch</span></span>
* <span data-ttu-id="e57a3-116">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-116">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e57a3-117">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e57a3-117">Az.Cdn</span></span>
* <span data-ttu-id="e57a3-118">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-118">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e57a3-119">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-119">Az.CognitiveServices</span></span>
* <span data-ttu-id="e57a3-120">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-120">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-121">Az.Compute</span></span>
* <span data-ttu-id="e57a3-122">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-122">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e57a3-123">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-123">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e57a3-124">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e57a3-124">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e57a3-125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e57a3-125">Az.DataFactory</span></span>
* <span data-ttu-id="e57a3-126">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="e57a3-126">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e57a3-127">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e57a3-127">Az.DataLakeStore</span></span>
* <span data-ttu-id="e57a3-128">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e57a3-129">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e57a3-129">Az.EventGrid</span></span>
* <span data-ttu-id="e57a3-130">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e57a3-130">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e57a3-131">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e57a3-131">Az.EventHub</span></span>
* <span data-ttu-id="e57a3-132">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-132">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e57a3-133">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e57a3-133">Az.HDInsight</span></span>
* <span data-ttu-id="e57a3-134">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-134">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e57a3-135">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e57a3-135">Az.IotHub</span></span>
* <span data-ttu-id="e57a3-136">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-136">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e57a3-137">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e57a3-137">Az.KeyVault</span></span>
* <span data-ttu-id="e57a3-138">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-138">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e57a3-139">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e57a3-139">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e57a3-140">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e57a3-140">Az.MachineLearning</span></span>
* <span data-ttu-id="e57a3-141">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-141">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e57a3-142">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e57a3-142">Az.Media</span></span>
* <span data-ttu-id="e57a3-143">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-143">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e57a3-144">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e57a3-144">Az.Monitor</span></span>
  * <span data-ttu-id="e57a3-145">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-145">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e57a3-146">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e57a3-146">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e57a3-147">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e57a3-147">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e57a3-148">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e57a3-148">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e57a3-149">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e57a3-149">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e57a3-150">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e57a3-150">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e57a3-151">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="e57a3-151">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e57a3-152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-152">Az.Network</span></span>
* <span data-ttu-id="e57a3-153">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-153">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e57a3-154">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e57a3-154">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e57a3-155">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e57a3-155">Az.NotificationHubs</span></span>
* <span data-ttu-id="e57a3-156">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e57a3-157">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e57a3-157">Az.OperationalInsights</span></span>
* <span data-ttu-id="e57a3-158">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-158">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e57a3-159">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e57a3-159">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e57a3-160">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-160">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e57a3-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="e57a3-162">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-162">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e57a3-163">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="e57a3-163">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e57a3-164">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="e57a3-164">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e57a3-165">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="e57a3-165">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e57a3-166">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e57a3-166">Az.RedisCache</span></span>
* <span data-ttu-id="e57a3-167">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-167">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-168">Az.Resources</span></span>
* <span data-ttu-id="e57a3-169">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e57a3-169">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-170">Az.Sql</span></span>
* <span data-ttu-id="e57a3-171">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="e57a3-171">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e57a3-172">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e57a3-173">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="e57a3-173">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e57a3-174">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="e57a3-174">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e57a3-175">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="e57a3-175">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e57a3-176">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="e57a3-176">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e57a3-177">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="e57a3-177">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e57a3-178">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e57a3-178">Az.Websites</span></span>
* <span data-ttu-id="e57a3-179">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="e57a3-179">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e57a3-180">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-180">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e57a3-181">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="e57a3-181">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e57a3-182">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="e57a3-182">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e57a3-183">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-183">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e57a3-184">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e57a3-184">Highlights since the last major release</span></span>
* <span data-ttu-id="e57a3-185">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="e57a3-185">General availability of `Az` module</span></span>
* <span data-ttu-id="e57a3-186">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e57a3-186">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e57a3-187">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e57a3-187">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e57a3-188">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-188">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e57a3-189">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="e57a3-189">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e57a3-190">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-190">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e57a3-191">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-191">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e57a3-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-192">Az.Accounts</span></span>
* <span data-ttu-id="e57a3-193">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="e57a3-193">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e57a3-194">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-194">Az.AnalysisServices</span></span>
* <span data-ttu-id="e57a3-195">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="e57a3-195">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e57a3-196">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="e57a3-196">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e57a3-197">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e57a3-197">Az.Automation</span></span>
* <span data-ttu-id="e57a3-198">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="e57a3-198">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e57a3-199">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="e57a3-199">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e57a3-200">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="e57a3-200">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-201">Az.Compute</span></span>
* <span data-ttu-id="e57a3-202">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e57a3-202">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e57a3-203">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="e57a3-203">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e57a3-204">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e57a3-204">Az.ContainerInstance</span></span>
* <span data-ttu-id="e57a3-205">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="e57a3-205">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e57a3-206">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e57a3-206">Az.DataFactory</span></span>
* <span data-ttu-id="e57a3-207">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="e57a3-207">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e57a3-208">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e57a3-208">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-209">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-209">Az.Resources</span></span>
* <span data-ttu-id="e57a3-210">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="e57a3-210">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e57a3-211">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="e57a3-211">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e57a3-212">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="e57a3-212">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e57a3-213">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e57a3-213">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e57a3-214">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="e57a3-214">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e57a3-215">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e57a3-215">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-216">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-216">Az.Sql</span></span>
* <span data-ttu-id="e57a3-217">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="e57a3-217">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e57a3-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e57a3-218">Az.Storage</span></span>
* <span data-ttu-id="e57a3-219">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="e57a3-219">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e57a3-220">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e57a3-220">New-AzStorageContext</span></span>
* <span data-ttu-id="e57a3-221">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="e57a3-221">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e57a3-222">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e57a3-222">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e57a3-223">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e57a3-223">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e57a3-224">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e57a3-224">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e57a3-225">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e57a3-225">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e57a3-226">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-226">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e57a3-227">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e57a3-227">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e57a3-228">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e57a3-228">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e57a3-229">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e57a3-229">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e57a3-230">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e57a3-230">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e57a3-231">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-231">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e57a3-232">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="e57a3-232">Highlights since the last major release</span></span>
* <span data-ttu-id="e57a3-233">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="e57a3-233">General availability of `Az` module</span></span>
* <span data-ttu-id="e57a3-234">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e57a3-234">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e57a3-235">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e57a3-235">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e57a3-236">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-236">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e57a3-237">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="e57a3-237">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e57a3-238">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-238">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e57a3-239">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-239">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e57a3-240">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e57a3-240">Az.Automation</span></span>
* <span data-ttu-id="e57a3-241">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="e57a3-241">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e57a3-242">動態分組</span><span class="sxs-lookup"><span data-stu-id="e57a3-242">Dynamic grouping</span></span>
    * <span data-ttu-id="e57a3-243">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="e57a3-243">Pre-Post script</span></span>
    * <span data-ttu-id="e57a3-244">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="e57a3-244">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-245">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-245">Az.Compute</span></span>
* <span data-ttu-id="e57a3-246">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-246">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e57a3-247">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="e57a3-247">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e57a3-248">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e57a3-248">Az.KeyVault</span></span>
* <span data-ttu-id="e57a3-249">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-249">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e57a3-250">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-250">Az.Network</span></span>
* <span data-ttu-id="e57a3-251">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-251">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e57a3-252">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="e57a3-252">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e57a3-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="e57a3-254">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="e57a3-254">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e57a3-255">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-255">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-256">Az.Resources</span></span>
* <span data-ttu-id="e57a3-257">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-257">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e57a3-258">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="e57a3-258">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-259">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-259">Az.Sql</span></span>
* <span data-ttu-id="e57a3-260">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="e57a3-260">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e57a3-261">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e57a3-261">Az.Storage</span></span>
* <span data-ttu-id="e57a3-262">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="e57a3-262">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e57a3-263">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e57a3-263">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e57a3-264">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e57a3-264">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e57a3-265">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e57a3-265">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e57a3-266">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e57a3-266">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e57a3-267">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e57a3-267">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e57a3-268">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e57a3-268">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e57a3-269">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e57a3-269">Az.Websites</span></span>
* <span data-ttu-id="e57a3-270">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="e57a3-270">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="e57a3-271">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-271">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e57a3-272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-272">Az.Accounts</span></span>
* <span data-ttu-id="e57a3-273">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-273">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e57a3-274">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="e57a3-274">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e57a3-275">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e57a3-275">Az.Automation</span></span>
* <span data-ttu-id="e57a3-276">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-276">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e57a3-277">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="e57a3-277">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e57a3-278">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="e57a3-278">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e57a3-279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e57a3-279">Az.Cdn</span></span>
* <span data-ttu-id="e57a3-280">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-280">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-281">Az.Compute</span></span>
* <span data-ttu-id="e57a3-282">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-282">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e57a3-283">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e57a3-283">Az.DataFactory</span></span>
* <span data-ttu-id="e57a3-284">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e57a3-284">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e57a3-285">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e57a3-285">Az.LogicApp</span></span>
* <span data-ttu-id="e57a3-286">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="e57a3-286">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e57a3-287">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-287">Az.Network</span></span>
* <span data-ttu-id="e57a3-288">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-288">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e57a3-289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-289">Az.RecoveryServices</span></span>
* <span data-ttu-id="e57a3-290">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-290">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e57a3-291">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="e57a3-291">SDK Update</span></span>
* <span data-ttu-id="e57a3-292">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="e57a3-292">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e57a3-293">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="e57a3-293">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-294">Az.Resources</span></span>
* <span data-ttu-id="e57a3-295">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-295">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e57a3-296">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e57a3-296">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e57a3-297">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-297">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e57a3-298">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e57a3-298">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e57a3-299">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-299">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e57a3-300">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e57a3-300">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-301">Az.Sql</span></span>
* <span data-ttu-id="e57a3-302">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="e57a3-302">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e57a3-303">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="e57a3-303">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e57a3-304">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e57a3-304">Az.Storage</span></span>
* <span data-ttu-id="e57a3-305">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e57a3-305">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e57a3-306">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-306">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e57a3-307">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-307">Az.AnalysisServices</span></span>
* <span data-ttu-id="e57a3-308">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-308">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e57a3-309">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e57a3-309">Az.Automation</span></span>
* <span data-ttu-id="e57a3-310">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="e57a3-310">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e57a3-311">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-311">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e57a3-312">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="e57a3-312">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e57a3-313">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-313">Az.CognitiveServices</span></span>
* <span data-ttu-id="e57a3-314">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="e57a3-314">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-315">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-315">Az.Compute</span></span>
* <span data-ttu-id="e57a3-316">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-316">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e57a3-317">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="e57a3-317">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e57a3-318">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-318">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e57a3-319">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="e57a3-319">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e57a3-320">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e57a3-320">Az.DataLakeStore</span></span>
* <span data-ttu-id="e57a3-321">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-321">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e57a3-322">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e57a3-322">Az.EventHub</span></span>
* <span data-ttu-id="e57a3-323">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="e57a3-323">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e57a3-324">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e57a3-324">Az.KeyVault</span></span>
* <span data-ttu-id="e57a3-325">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="e57a3-325">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e57a3-326">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e57a3-326">Az.LogicApp</span></span>
* <span data-ttu-id="e57a3-327">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="e57a3-327">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e57a3-328">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="e57a3-328">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e57a3-329">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-329">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e57a3-330">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e57a3-330">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e57a3-331">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e57a3-331">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e57a3-332">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e57a3-332">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e57a3-333">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e57a3-333">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e57a3-334">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-334">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e57a3-335">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e57a3-335">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e57a3-336">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e57a3-336">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e57a3-337">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e57a3-337">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e57a3-338">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e57a3-338">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e57a3-339">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="e57a3-339">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e57a3-340">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e57a3-340">Az.Monitor</span></span>
* <span data-ttu-id="e57a3-341">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="e57a3-341">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e57a3-342">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-342">Az.Network</span></span>
* <span data-ttu-id="e57a3-343">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="e57a3-343">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e57a3-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e57a3-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="e57a3-345">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="e57a3-345">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e57a3-346">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="e57a3-346">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="e57a3-347">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="e57a3-347">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-348">Az.Resources</span></span>
* <span data-ttu-id="e57a3-349">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-349">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e57a3-350">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-350">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e57a3-351">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-351">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e57a3-352">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="e57a3-352">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-353">Az.Sql</span></span>
* <span data-ttu-id="e57a3-354">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-354">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e57a3-355">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="e57a3-355">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e57a3-356">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e57a3-356">Az.Websites</span></span>
* <span data-ttu-id="e57a3-357">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="e57a3-357">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e57a3-358">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-358">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e57a3-359">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-359">Az.Accounts</span></span>
* <span data-ttu-id="e57a3-360">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e57a3-360">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e57a3-361">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-361">Az.AnalysisServices</span></span>
<span data-ttu-id="e57a3-362">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="e57a3-362">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-363">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-363">Az.Compute</span></span>
* <span data-ttu-id="e57a3-364">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-364">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e57a3-365">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="e57a3-365">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e57a3-366">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="e57a3-366">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e57a3-367">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-367">Az.RecoveryServices</span></span>
<span data-ttu-id="e57a3-368">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="e57a3-368">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-369">Az.Resources</span></span>
* <span data-ttu-id="e57a3-370">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="e57a3-370">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="e57a3-371">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e57a3-371">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e57a3-372">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-372">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="e57a3-373">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e57a3-373">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-374">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-374">Az.Sql</span></span>
* <span data-ttu-id="e57a3-375">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e57a3-375">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e57a3-376">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-376">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e57a3-377">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="e57a3-377">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e57a3-378">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-378">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e57a3-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-379">Az.Accounts</span></span>
* <span data-ttu-id="e57a3-380">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="e57a3-380">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e57a3-381">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-381">Az.AnalysisServices</span></span>
* <span data-ttu-id="e57a3-382">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="e57a3-382">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e57a3-383">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-383">Az.RecoveryServices</span></span>
* <span data-ttu-id="e57a3-384">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="e57a3-384">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e57a3-385">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-385">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e57a3-386">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-386">Az.Accounts</span></span>
* <span data-ttu-id="e57a3-387">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="e57a3-387">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e57a3-388">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-388">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e57a3-389">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="e57a3-389">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e57a3-390">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e57a3-390">Az.Aks</span></span>
* <span data-ttu-id="e57a3-391">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-391">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e57a3-392">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e57a3-392">Az.Automation</span></span>
* <span data-ttu-id="e57a3-393">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-393">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e57a3-394">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-394">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e57a3-395">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e57a3-395">Az.Cdn</span></span>
* <span data-ttu-id="e57a3-396">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-396">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-397">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-397">Az.Compute</span></span>
* <span data-ttu-id="e57a3-398">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-398">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e57a3-399">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e57a3-399">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e57a3-400">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="e57a3-400">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e57a3-401">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e57a3-401">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e57a3-402">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-402">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e57a3-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e57a3-403">Az.DataFactory</span></span>
* <span data-ttu-id="e57a3-404">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e57a3-404">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e57a3-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e57a3-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="e57a3-406">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-406">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e57a3-407">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e57a3-407">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e57a3-408">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-408">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e57a3-409">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e57a3-409">Az.IotHub</span></span>
* <span data-ttu-id="e57a3-410">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e57a3-410">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e57a3-411">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e57a3-411">Az.KeyVault</span></span>
* <span data-ttu-id="e57a3-412">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-412">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e57a3-413">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-413">Az.Network</span></span>
* <span data-ttu-id="e57a3-414">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-414">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-415">Az.Resources</span></span>
* <span data-ttu-id="e57a3-416">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="e57a3-416">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e57a3-417">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-417">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e57a3-418">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="e57a3-418">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e57a3-419">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-419">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e57a3-420">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-420">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e57a3-421">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-421">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e57a3-422">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e57a3-422">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e57a3-423">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e57a3-423">Az.ServiceFabric</span></span>
* <span data-ttu-id="e57a3-424">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e57a3-424">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e57a3-425">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e57a3-425">Fix some error messages.</span></span>
* <span data-ttu-id="e57a3-426">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="e57a3-426">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e57a3-427">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="e57a3-427">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e57a3-428">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e57a3-428">Az.SignalR</span></span>
* <span data-ttu-id="e57a3-429">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-429">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-430">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-430">Az.Sql</span></span>
* <span data-ttu-id="e57a3-431">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-431">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e57a3-432">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="e57a3-432">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e57a3-433">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-433">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e57a3-434">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="e57a3-434">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e57a3-435">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e57a3-435">Az.Storage</span></span>
* <span data-ttu-id="e57a3-436">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-436">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e57a3-437">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="e57a3-437">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e57a3-438">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e57a3-438">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e57a3-439">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e57a3-439">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e57a3-440">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e57a3-440">Az.TrafficManager</span></span>
* <span data-ttu-id="e57a3-441">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-441">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e57a3-442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e57a3-442">Az.Websites</span></span>
* <span data-ttu-id="e57a3-443">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-443">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e57a3-444">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="e57a3-444">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e57a3-445">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="e57a3-445">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e57a3-446">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-446">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e57a3-447">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-447">Az.Accounts</span></span>
* <span data-ttu-id="e57a3-448">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e57a3-448">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-449">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-449">Az.Compute</span></span>
* <span data-ttu-id="e57a3-450">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="e57a3-450">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e57a3-451">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="e57a3-451">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e57a3-452">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-452">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e57a3-453">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e57a3-453">Az.DataLakeStore</span></span>
* <span data-ttu-id="e57a3-454">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="e57a3-454">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e57a3-455">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="e57a3-455">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e57a3-456">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e57a3-456">Az.EventGrid</span></span>
* <span data-ttu-id="e57a3-457">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e57a3-457">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e57a3-458">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="e57a3-458">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e57a3-459">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="e57a3-459">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e57a3-460">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="e57a3-460">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e57a3-461">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="e57a3-461">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e57a3-462">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="e57a3-462">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e57a3-463">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="e57a3-463">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e57a3-464">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="e57a3-464">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e57a3-465">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="e57a3-465">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e57a3-466">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="e57a3-466">Dead letter endpoint.</span></span>
* <span data-ttu-id="e57a3-467">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="e57a3-467">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e57a3-468">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="e57a3-468">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e57a3-469">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e57a3-469">Az.IotHub</span></span>
* <span data-ttu-id="e57a3-470">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="e57a3-470">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e57a3-471">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e57a3-471">Az.LogicApp</span></span>
* <span data-ttu-id="e57a3-472">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="e57a3-472">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-473">Az.Resources</span></span>
* <span data-ttu-id="e57a3-474">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-474">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e57a3-475">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e57a3-475">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e57a3-476">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="e57a3-476">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e57a3-477">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="e57a3-477">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e57a3-478">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="e57a3-478">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e57a3-479">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e57a3-479">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e57a3-480">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e57a3-480">Az.SignalR</span></span>
* <span data-ttu-id="e57a3-481">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-481">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-482">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-482">Az.Sql</span></span>
* <span data-ttu-id="e57a3-483">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="e57a3-483">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e57a3-484">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e57a3-484">Az.Storage</span></span>
* <span data-ttu-id="e57a3-485">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="e57a3-485">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e57a3-486">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e57a3-486">New-AzStorageContext</span></span>
* <span data-ttu-id="e57a3-487">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="e57a3-487">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e57a3-488">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e57a3-488">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e57a3-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e57a3-489">Az.Websites</span></span>
* <span data-ttu-id="e57a3-490">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="e57a3-490">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e57a3-491">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-491">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e57a3-492">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-492">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e57a3-493">一般</span><span class="sxs-lookup"><span data-stu-id="e57a3-493">General</span></span>

- <span data-ttu-id="e57a3-494">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="e57a3-494">General Availability of Az Module</span></span>
- <span data-ttu-id="e57a3-495">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="e57a3-495">Online help for each module</span></span>
- <span data-ttu-id="e57a3-496">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e57a3-496">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e57a3-497">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-497">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e57a3-498">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-498">Az.Accounts</span></span>
- <span data-ttu-id="e57a3-499">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="e57a3-499">Changed from Az.Profile</span></span>
- <span data-ttu-id="e57a3-500">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="e57a3-500">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e57a3-501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e57a3-501">Az.ApiManagement</span></span>
- <span data-ttu-id="e57a3-502">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="e57a3-502">Fixes for #7002</span></span>
- <span data-ttu-id="e57a3-503">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-503">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e57a3-504">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e57a3-504">Az.Batch</span></span>
- <span data-ttu-id="e57a3-505">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="e57a3-505">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e57a3-506">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="e57a3-506">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e57a3-507">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-507">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e57a3-508">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e57a3-508">Az.Billing</span></span>
- <span data-ttu-id="e57a3-509">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-509">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e57a3-510">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-510">Az.CognitivServices</span></span>
- <span data-ttu-id="e57a3-511">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="e57a3-511">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e57a3-512">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="e57a3-512">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e57a3-513">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e57a3-513">Az.ContainerInstance</span></span>
- <span data-ttu-id="e57a3-514">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-514">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e57a3-515">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e57a3-515">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e57a3-516">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-516">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e57a3-517">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e57a3-517">Az.DataLakeStore</span></span>
- <span data-ttu-id="e57a3-518">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e57a3-519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e57a3-519">Az.Monitor</span></span>
- <span data-ttu-id="e57a3-520">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-520">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e57a3-521">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e57a3-521">Az.KeyVault</span></span>
- <span data-ttu-id="e57a3-522">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="e57a3-522">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e57a3-523">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e57a3-523">Az.MachineLearning</span></span>
- <span data-ttu-id="e57a3-524">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-524">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e57a3-525">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e57a3-525">Az.Media</span></span>
- <span data-ttu-id="e57a3-526">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="e57a3-526">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e57a3-527">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-527">Az.Network</span></span>
<span data-ttu-id="e57a3-528">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-528">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e57a3-529">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e57a3-529">New cmdlets added:</span></span>
        - <span data-ttu-id="e57a3-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e57a3-530">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e57a3-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e57a3-531">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e57a3-532">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e57a3-532">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e57a3-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e57a3-533">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e57a3-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e57a3-534">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e57a3-535">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e57a3-535">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e57a3-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e57a3-536">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e57a3-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e57a3-537">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e57a3-538">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e57a3-538">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e57a3-539">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e57a3-539">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e57a3-540">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e57a3-540">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e57a3-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e57a3-541">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e57a3-542">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e57a3-542">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e57a3-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e57a3-543">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e57a3-544">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="e57a3-544">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e57a3-545">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-545">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e57a3-546">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e57a3-546">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e57a3-547">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e57a3-547">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e57a3-548">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e57a3-548">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e57a3-549">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-549">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e57a3-550">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-550">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e57a3-551">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e57a3-551">Az.OperationalInsights</span></span>
- <span data-ttu-id="e57a3-552">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e57a3-553">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e57a3-553">Az.Profile</span></span>
- <span data-ttu-id="e57a3-554">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e57a3-554">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e57a3-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-555">Az.RecoveryServices</span></span>
- <span data-ttu-id="e57a3-556">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-556">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e57a3-557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-557">Az.Resources</span></span>
- <span data-ttu-id="e57a3-558">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-558">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e57a3-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e57a3-559">Az.ServiceFabric</span></span>
- <span data-ttu-id="e57a3-560">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="e57a3-560">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e57a3-561">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-561">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e57a3-562">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e57a3-562">Az.SIgnalR</span></span>
- <span data-ttu-id="e57a3-563">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="e57a3-563">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e57a3-564">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-564">Az.Sql</span></span>
- <span data-ttu-id="e57a3-565">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="e57a3-565">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e57a3-566">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="e57a3-566">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e57a3-567">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-567">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e57a3-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e57a3-568">Az.Storage</span></span>
- <span data-ttu-id="e57a3-569">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-569">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e57a3-570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e57a3-570">Az.Websites</span></span>
- <span data-ttu-id="e57a3-571">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="e57a3-571">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e57a3-572">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-572">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e57a3-573">一般</span><span class="sxs-lookup"><span data-stu-id="e57a3-573">General</span></span>

* <span data-ttu-id="e57a3-574">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="e57a3-574">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e57a3-575">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-575">Az.Compute</span></span>

* <span data-ttu-id="e57a3-576">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="e57a3-576">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e57a3-577">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e57a3-577">Az.DataLakeStore</span></span>

* <span data-ttu-id="e57a3-578">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="e57a3-578">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e57a3-579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e57a3-579">Az.FrontDoor</span></span>

* <span data-ttu-id="e57a3-580">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="e57a3-580">Fixed some broken links</span></span>
    - <span data-ttu-id="e57a3-581">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="e57a3-581">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e57a3-582">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="e57a3-582">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e57a3-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-583">Az.RecoveryServices</span></span>

* <span data-ttu-id="e57a3-584">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="e57a3-584">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e57a3-585">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="e57a3-585">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e57a3-586">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-586">Az.Resources</span></span>

* <span data-ttu-id="e57a3-587">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e57a3-587">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e57a3-588">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="e57a3-588">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e57a3-589">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-589">Az.Sql</span></span>

* <span data-ttu-id="e57a3-590">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="e57a3-590">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e57a3-591">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-591">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e57a3-592">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="e57a3-592">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e57a3-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e57a3-593">Az.Storage</span></span>

* <span data-ttu-id="e57a3-594">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="e57a3-594">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e57a3-595">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="e57a3-595">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e57a3-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e57a3-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e57a3-597">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="e57a3-597">Support Static Website configuration</span></span>
    - <span data-ttu-id="e57a3-598">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e57a3-598">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e57a3-599">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e57a3-599">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e57a3-600">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e57a3-600">Az.Websites</span></span>

* <span data-ttu-id="e57a3-601">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e57a3-601">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="e57a3-602">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="e57a3-602">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e57a3-603">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="e57a3-603">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e57a3-604">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-604">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e57a3-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e57a3-605">Az.ApiManagement</span></span>
* <span data-ttu-id="e57a3-606">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="e57a3-606">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e57a3-607">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e57a3-607">Az.Automation</span></span>
* <span data-ttu-id="e57a3-608">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-608">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e57a3-609">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-609">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e57a3-610">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-610">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e57a3-611">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-611">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e57a3-612">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="e57a3-612">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e57a3-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-613">Az.Compute</span></span>
* <span data-ttu-id="e57a3-614">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-614">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e57a3-615">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="e57a3-615">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e57a3-616">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e57a3-616">Az.ContainerInstance</span></span>
* <span data-ttu-id="e57a3-617">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="e57a3-617">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e57a3-618">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e57a3-618">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e57a3-619">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="e57a3-619">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e57a3-620">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-620">Az.Network</span></span>
* <span data-ttu-id="e57a3-621">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e57a3-621">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e57a3-622">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="e57a3-622">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e57a3-623">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="e57a3-623">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="e57a3-624">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-624">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e57a3-625">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e57a3-625">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e57a3-626">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="e57a3-626">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e57a3-627">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="e57a3-627">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e57a3-628">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e57a3-628">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e57a3-629">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="e57a3-629">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e57a3-630">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="e57a3-630">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e57a3-631">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e57a3-631">Az.Relay</span></span>
* <span data-ttu-id="e57a3-632">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="e57a3-632">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e57a3-633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-633">Az.Resources</span></span>
* <span data-ttu-id="e57a3-634">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="e57a3-634">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e57a3-635">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="e57a3-635">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e57a3-636">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="e57a3-636">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e57a3-637">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e57a3-637">Az.ServiceFabric</span></span>
* <span data-ttu-id="e57a3-638">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="e57a3-638">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e57a3-639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-639">Az.Sql</span></span>
* <span data-ttu-id="e57a3-640">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-640">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e57a3-641">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e57a3-641">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e57a3-642">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e57a3-642">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e57a3-643">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e57a3-643">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e57a3-644">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e57a3-644">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e57a3-645">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e57a3-645">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e57a3-646">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e57a3-646">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e57a3-647">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e57a3-647">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e57a3-648">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e57a3-648">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e57a3-649">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="e57a3-649">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e57a3-650">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="e57a3-650">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e57a3-651">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="e57a3-651">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e57a3-652">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="e57a3-652">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e57a3-653">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="e57a3-653">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e57a3-654">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="e57a3-654">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e57a3-655">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="e57a3-655">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e57a3-656">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-656">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e57a3-657">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-657">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e57a3-658">一般</span><span class="sxs-lookup"><span data-stu-id="e57a3-658">General</span></span>
* <span data-ttu-id="e57a3-659">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="e57a3-659">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e57a3-660">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e57a3-660">Az.Profile</span></span>
* <span data-ttu-id="e57a3-661">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e57a3-661">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e57a3-662">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="e57a3-662">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e57a3-663">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="e57a3-663">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e57a3-664">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e57a3-664">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e57a3-665">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-665">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e57a3-666">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-666">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e57a3-667">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-667">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e57a3-668">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-668">Az.CognitiveServices</span></span>
* <span data-ttu-id="e57a3-669">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="e57a3-669">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-670">Az.Compute</span></span>
* <span data-ttu-id="e57a3-671">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-671">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e57a3-672">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e57a3-672">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e57a3-673">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="e57a3-673">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e57a3-674">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e57a3-674">Az.DataLakeStore</span></span>
* <span data-ttu-id="e57a3-675">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="e57a3-675">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e57a3-676">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="e57a3-676">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e57a3-677">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e57a3-677">Az.Insights</span></span>
* <span data-ttu-id="e57a3-678">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="e57a3-678">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e57a3-679">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="e57a3-679">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e57a3-680">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="e57a3-680">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e57a3-681">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="e57a3-681">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e57a3-682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-682">Az.Network</span></span>
* <span data-ttu-id="e57a3-683">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="e57a3-683">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e57a3-684">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e57a3-684">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e57a3-685">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e57a3-685">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e57a3-686">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e57a3-686">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e57a3-687">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e57a3-687">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e57a3-688">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e57a3-688">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e57a3-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e57a3-689">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e57a3-690">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e57a3-690">Az.PolicyInsights</span></span>
* <span data-ttu-id="e57a3-691">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-691">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-692">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-692">Az.Resources</span></span>
* <span data-ttu-id="e57a3-693">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e57a3-693">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e57a3-694">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="e57a3-694">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e57a3-695">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e57a3-695">Az.ServiceBus</span></span>
* <span data-ttu-id="e57a3-696">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="e57a3-696">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e57a3-697">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e57a3-697">Az.ServiceFabric</span></span>
* <span data-ttu-id="e57a3-698">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="e57a3-698">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e57a3-699">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="e57a3-699">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e57a3-700">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="e57a3-700">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e57a3-701">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="e57a3-701">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e57a3-702">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="e57a3-702">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e57a3-703">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-703">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e57a3-704">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e57a3-704">Az.Profile</span></span>
* <span data-ttu-id="e57a3-705">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-705">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e57a3-706">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e57a3-706">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-707">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-707">Az.Compute</span></span>
* <span data-ttu-id="e57a3-708">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="e57a3-708">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e57a3-709">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e57a3-709">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e57a3-710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e57a3-710">Az.DataLakeStore</span></span>
* <span data-ttu-id="e57a3-711">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="e57a3-711">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e57a3-712">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e57a3-712">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e57a3-713">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="e57a3-713">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e57a3-714">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e57a3-714">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e57a3-715">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="e57a3-715">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e57a3-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-716">Az.Network</span></span>
* <span data-ttu-id="e57a3-717">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="e57a3-717">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e57a3-718">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e57a3-718">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-719">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-719">Az.Resources</span></span>
* <span data-ttu-id="e57a3-720">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="e57a3-720">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e57a3-721">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="e57a3-721">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e57a3-722">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-722">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e57a3-723">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e57a3-723">Azure.Storage</span></span>
* <span data-ttu-id="e57a3-724">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-724">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e57a3-725">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e57a3-725">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e57a3-726">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e57a3-726">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e57a3-727">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="e57a3-727">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e57a3-728">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e57a3-728">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e57a3-729">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e57a3-729">Az.CognitiveServices</span></span>
* <span data-ttu-id="e57a3-730">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="e57a3-730">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e57a3-731">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e57a3-731">Az.Compute</span></span>
* <span data-ttu-id="e57a3-732">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="e57a3-732">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e57a3-733">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="e57a3-733">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e57a3-734">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="e57a3-734">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e57a3-735">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e57a3-735">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e57a3-736">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="e57a3-736">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e57a3-737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e57a3-737">Az.Network</span></span>
* <span data-ttu-id="e57a3-738">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="e57a3-738">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e57a3-739">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-739">new cmdlets added</span></span>
    - <span data-ttu-id="e57a3-740">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e57a3-740">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e57a3-741">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e57a3-741">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e57a3-742">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e57a3-742">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e57a3-743">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e57a3-743">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e57a3-744">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e57a3-744">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e57a3-745">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e57a3-745">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e57a3-746">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="e57a3-746">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e57a3-747">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-747">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e57a3-748">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e57a3-748">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e57a3-749">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e57a3-749">Az.RedisCache</span></span>
* <span data-ttu-id="e57a3-750">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="e57a3-750">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e57a3-751">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="e57a3-751">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e57a3-752">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e57a3-752">Az.Resources</span></span>
* <span data-ttu-id="e57a3-753">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e57a3-753">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e57a3-754">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="e57a3-754">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e57a3-755">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e57a3-755">Az.Sql</span></span>
* <span data-ttu-id="e57a3-756">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="e57a3-756">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e57a3-757">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e57a3-757">Az.Websites</span></span>
* <span data-ttu-id="e57a3-758">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="e57a3-758">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e57a3-759">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="e57a3-759">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e57a3-760">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="e57a3-760">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e57a3-761">初始版本</span><span class="sxs-lookup"><span data-stu-id="e57a3-761">Initial Release</span></span>
