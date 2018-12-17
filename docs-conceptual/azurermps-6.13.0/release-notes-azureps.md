---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/13/2018
ms.locfileid: "53218216"
---
# <a name="release-notes"></a><span data-ttu-id="47836-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="47836-103">Release notes</span></span>

<span data-ttu-id="47836-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="47836-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="47836-105">6.13.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="47836-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47836-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-106">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-107">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="47836-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47836-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47836-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47836-109">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="47836-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="47836-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="47836-110">AzureRM.Automation</span></span>
* <span data-ttu-id="47836-111">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="47836-112">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="47836-113">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="47836-114">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="47836-115">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="47836-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-116">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-117">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="47836-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="47836-118">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="47836-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="47836-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="47836-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="47836-120">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="47836-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="47836-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="47836-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="47836-122">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="47836-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-123">AzureRM.Network</span></span>
* <span data-ttu-id="47836-124">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="47836-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="47836-125">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="47836-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="47836-126">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="47836-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="47836-127">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="47836-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47836-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47836-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47836-129">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="47836-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="47836-130">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="47836-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="47836-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="47836-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="47836-132">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="47836-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="47836-133">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="47836-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="47836-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="47836-134">AzureRM.Relay</span></span>
* <span data-ttu-id="47836-135">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="47836-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-136">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-137">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="47836-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="47836-138">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="47836-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="47836-139">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="47836-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47836-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47836-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47836-141">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="47836-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47836-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-142">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-143">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="47836-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47836-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47836-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47836-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47836-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47836-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47836-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47836-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47836-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="47836-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47836-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="47836-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47836-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="47836-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47836-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="47836-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="47836-152">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="47836-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="47836-153">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="47836-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="47836-154">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="47836-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="47836-155">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="47836-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="47836-156">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="47836-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="47836-157">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="47836-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="47836-158">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="47836-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="47836-159">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="47836-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="47836-160">6.12.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="47836-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47836-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-161">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-162">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="47836-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="47836-163">將 Cmdlet Connect-AzureRmAccount 中的 param TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="47836-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="47836-164">更新 Connect-AzureRmAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="47836-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="47836-165">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="47836-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="47836-166">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="47836-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="47836-167">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="47836-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="47836-168">修正若未連線，'Disconnect-AzureRmAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="47836-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="47836-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="47836-169">AzureRM.Automation</span></span>
* <span data-ttu-id="47836-170">已將 Cmdlet DLL 檔案名稱重新命名為 Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="47836-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="47836-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47836-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="47836-172">新增 Get-AzureRmCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="47836-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-173">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-174">新增 Add-AzureRmVmssVMDataDisk 和 Remove-AzureRmVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="47836-175">Get-AzureRmVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="47836-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="47836-176">已修正 SetAzureRmVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47836-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47836-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47836-178">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="47836-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="47836-179">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="47836-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="47836-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="47836-180">AzureRM.Insights</span></span>
* <span data-ttu-id="47836-181">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="47836-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="47836-182">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="47836-183">已修正問題 #7513 [Insights] Set-AzureRMDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="47836-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="47836-184">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="47836-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-185">AzureRM.Network</span></span>
* <span data-ttu-id="47836-186">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="47836-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="47836-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="47836-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="47836-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="47836-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="47836-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="47836-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="47836-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="47836-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="47836-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="47836-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="47836-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="47836-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="47836-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47836-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="47836-194">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47836-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47836-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47836-196">已新增在復原服務中共用 Azure 檔案的支援。</span><span class="sxs-lookup"><span data-stu-id="47836-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-197">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-198">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="47836-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="47836-199">允許使用 'Get-AzureRmResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="47836-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47836-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47836-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47836-201">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="47836-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47836-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47836-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47836-203">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="47836-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="47836-204">修正 'Add-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="47836-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="47836-205">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="47836-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="47836-206">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="47836-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="47836-207">修正 'Update-AzureRmServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="47836-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="47836-208">6.11.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="47836-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47836-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-209">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-210">修正 CloudShell 中 Get-AzureRmSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="47836-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="47836-211">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="47836-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="47836-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="47836-212">AzureRM.Backup</span></span>
* <span data-ttu-id="47836-213">淘汰的 Azure 備份 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-214">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-215">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzureRmVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="47836-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="47836-216">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47836-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47836-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47836-218">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="47836-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="47836-219">Get-AzureRmDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="47836-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="47836-220">Add-AzureRmDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="47836-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="47836-221">Set-AzureRmDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="47836-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="47836-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="47836-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-223">AzureRM.Network</span></span>
* <span data-ttu-id="47836-224">更新 Cmdlet Test-AzureRmNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="47836-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="47836-225">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-226">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-227">修正當 Get-AzureRMRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="47836-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="47836-228">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="47836-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="47836-229">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="47836-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="47836-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-230">Azure.Storage</span></span>
* <span data-ttu-id="47836-231">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="47836-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="47836-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="47836-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="47836-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="47836-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="47836-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47836-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="47836-235">在沒有現有帳戶的情況下支援 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="47836-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-236">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-237">修正 Get-AzureRmVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="47836-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="47836-238">已將 'SimpleParameterSet' 的範例新增到 New-AzureRmVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="47836-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="47836-239">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="47836-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="47836-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47836-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="47836-241">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="47836-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-242">AzureRM.Network</span></span>
* <span data-ttu-id="47836-243">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="47836-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="47836-244">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-244">new cmdlets added</span></span>
    - <span data-ttu-id="47836-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47836-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="47836-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47836-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="47836-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47836-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="47836-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47836-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="47836-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="47836-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="47836-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="47836-251">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="47836-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="47836-252">已新增 New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap 和 Remove-AzureRmVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="47836-253">已新增 Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig 和 Remove-AzureRmNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="47836-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47836-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="47836-255">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="47836-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="47836-256">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="47836-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-257">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-258">將遺漏的 -Mode 參數新增至 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="47836-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="47836-259">修正 Get-AzureRmProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="47836-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47836-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-260">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-261">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="47836-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="47836-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-262">AzureRM.Storage</span></span>
* <span data-ttu-id="47836-263">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="47836-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="47836-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="47836-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47836-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47836-265">AzureRM.Websites</span></span>
* <span data-ttu-id="47836-266">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="47836-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="47836-267">新 Cmdlet New-AzureRMWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="47836-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="47836-268">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="47836-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47836-269">一般</span><span class="sxs-lookup"><span data-stu-id="47836-269">General</span></span>
* <span data-ttu-id="47836-270">已將 AzureRM.SignalR 新增至 AzureRM 彙總模組</span><span class="sxs-lookup"><span data-stu-id="47836-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="47836-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-271">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-272">儲存體通用程式碼的小幅變更</span><span class="sxs-lookup"><span data-stu-id="47836-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="47836-273">已更新說明檔以包含完整的參數類型。</span><span class="sxs-lookup"><span data-stu-id="47836-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="47836-274">已變更 - 非強制性的 ServicePrincipal 位在 ServicePrincipalCertificateWithSubscriptionId 參數集</span><span class="sxs-lookup"><span data-stu-id="47836-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="47836-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-275">Azure.Storage</span></span>
* <span data-ttu-id="47836-276">支援使用 OAuth 建立儲存體內容。</span><span class="sxs-lookup"><span data-stu-id="47836-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="47836-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="47836-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="47836-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="47836-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="47836-279">已在 CDN 定價 SKU 中新增 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="47836-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="47836-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-280">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-281">將金鑰保存庫和儲存體上的相依性移至一般相依性</span><span class="sxs-lookup"><span data-stu-id="47836-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="47836-282">對 AEM Cmdlet 新增更多的虛擬機器大小支援</span><span class="sxs-lookup"><span data-stu-id="47836-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="47836-283">將 PublicIPPrefix 參數新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="47836-284">將 ResourceId 參數新增至 Invoke-AzureRmVMRunCommand Cmdelt</span><span class="sxs-lookup"><span data-stu-id="47836-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="47836-285">新增 Invoke-AzureRmVmssVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="47836-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="47836-286">AzureRM.Dns</span></span>
* <span data-ttu-id="47836-287">已新增建立 DNS 記錄時的別名記錄支援</span><span class="sxs-lookup"><span data-stu-id="47836-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="47836-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="47836-288">AzureRM.Insights</span></span>
* <span data-ttu-id="47836-289">已修正問題 #6833 和 #7102 (診斷設定區域)</span><span class="sxs-lookup"><span data-stu-id="47836-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="47836-290">建立和列出/取得診斷設定時的預設名稱問題 (例如 'service')</span><span class="sxs-lookup"><span data-stu-id="47836-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="47836-291">以類別建立診斷設定的問題</span><span class="sxs-lookup"><span data-stu-id="47836-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="47836-292">已新增計量時間粒紋參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="47836-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="47836-293">Timegrains 參數還是可用 (這是非中斷性變更)，但會在後端中遭到忽略，因為只有 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="47836-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-294">AzureRM.Network</span></span>
* <span data-ttu-id="47836-295">LoadBalancer Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="47836-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="47836-296">LoadBalancerInboundNatPoolConfig：已新增 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="47836-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="47836-297">LoadBalancerInboundNatRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="47836-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="47836-298">LoadBalancerRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="47836-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="47836-299">LoadBalancerProbeConfig：已為 Protocol 參數新增 "Https" 值的支援</span><span class="sxs-lookup"><span data-stu-id="47836-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="47836-300">已為新 LoadBalancer 的子資源 OutboundRule 新增命令</span><span class="sxs-lookup"><span data-stu-id="47836-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="47836-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47836-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="47836-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47836-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="47836-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47836-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="47836-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47836-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="47836-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47836-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="47836-306">已為 PSNetworkInterface 新增 HostedWorkloads 屬性</span><span class="sxs-lookup"><span data-stu-id="47836-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="47836-307">已新增功能的新 Cmdlet：透過 ARM 的 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="47836-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="47836-308">已新增 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="47836-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="47836-309">已新增 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="47836-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="47836-310">已新增 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="47836-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="47836-311">已新增 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="47836-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="47836-312">已新增 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="47836-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="47836-313">已新增 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="47836-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="47836-314">已新增 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="47836-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="47836-315">已新增 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="47836-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="47836-316">已新增 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="47836-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="47836-317">已新增 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="47836-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="47836-318">已在應用程式閘道中新增受信任根憑證和自動調整組態的支援</span><span class="sxs-lookup"><span data-stu-id="47836-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="47836-319">已新增的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="47836-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="47836-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47836-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47836-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47836-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47836-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="47836-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="47836-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="47836-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="47836-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="47836-329">已使用選擇性參數 TrustedRootCertificate 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="47836-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47836-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="47836-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47836-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="47836-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47836-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="47836-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47836-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="47836-334">已使用選擇性參數 AutoscaleConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="47836-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47836-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="47836-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47836-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="47836-337">為介面端點 Get-AzureInterfaceEndpoint 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="47836-338">已在子網路中新增多個位址前置詞的支援。</span><span class="sxs-lookup"><span data-stu-id="47836-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="47836-339">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="47836-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="47836-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="47836-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="47836-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="47836-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="47836-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="47836-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="47836-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="47836-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="47836-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="47836-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="47836-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="47836-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="47836-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="47836-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="47836-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="47836-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="47836-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="47836-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="47836-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="47836-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="47836-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="47836-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="47836-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="47836-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="47836-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="47836-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="47836-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="47836-359">為子網路委派新增 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="47836-360">New-AzureRmDelegation：建立可新增至子網路的新委派</span><span class="sxs-lookup"><span data-stu-id="47836-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="47836-361">Remove-AzureRmDelegation：用於子網路，可從該子網路中移除提供的委派名稱</span><span class="sxs-lookup"><span data-stu-id="47836-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="47836-362">Add-AzureRmDelegation：用於子網路，可將提供的服務名稱新增為該子網路的委派</span><span class="sxs-lookup"><span data-stu-id="47836-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="47836-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="47836-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="47836-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="47836-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="47836-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="47836-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="47836-366">支援受控磁碟</span><span class="sxs-lookup"><span data-stu-id="47836-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="47836-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47836-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="47836-368">已更新深入解析相依性。</span><span class="sxs-lookup"><span data-stu-id="47836-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-369">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-370">使用新參數 RollbackAction 更新 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="47836-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="47836-371">使用新參數新增 OnErrorDeployment 的支援。</span><span class="sxs-lookup"><span data-stu-id="47836-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="47836-372">支援原則指派上的受控識別。</span><span class="sxs-lookup"><span data-stu-id="47836-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="47836-373">以 'New-AzureRmPolicyAssignment' 指派原則時不再需要具有預設值的參數</span><span class="sxs-lookup"><span data-stu-id="47836-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="47836-374">新增 Get-AzureRmPolicyAlias Cmdlet 來擷取原則別名</span><span class="sxs-lookup"><span data-stu-id="47836-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47836-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47836-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47836-376">已修正問題 #7161</span><span class="sxs-lookup"><span data-stu-id="47836-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="47836-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="47836-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="47836-378">將 SKU 名稱更新為 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="47836-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="47836-379">將版本欄位新增至 PSSignalRResource 物件，以及將連接字串新增至 PSSignalRKeys 物件。</span><span class="sxs-lookup"><span data-stu-id="47836-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="47836-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-380">AzureRM.Storage</span></span>
* <span data-ttu-id="47836-381">在 AzureRm.Storage 中支援不變原則</span><span class="sxs-lookup"><span data-stu-id="47836-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="47836-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="47836-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="47836-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47836-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="47836-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47836-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="47836-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47836-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="47836-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47836-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="47836-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="47836-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="47836-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="47836-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="47836-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47836-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="47836-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47836-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="47836-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47836-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="47836-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47836-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47836-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47836-393">AzureRM.Websites</span></span>
* <span data-ttu-id="47836-394">已新增兩個新的 Cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="47836-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="47836-395">New-AzureRmAppServicePlan - 已新增 HyperV 切換以使用 Windows 容器建立 App Service 方案</span><span class="sxs-lookup"><span data-stu-id="47836-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="47836-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 已新增參數 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) 來建立和管理 Windows 容器應用程式</span><span class="sxs-lookup"><span data-stu-id="47836-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="47836-397">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="47836-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47836-398">一般</span><span class="sxs-lookup"><span data-stu-id="47836-398">General</span></span>
* <span data-ttu-id="47836-399">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="47836-400">已更新通用執行階段組件</span><span class="sxs-lookup"><span data-stu-id="47836-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47836-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47836-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47836-402">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="47836-403">已修正的問題 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="47836-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="47836-404">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlets 目前處理相對路徑</span><span class="sxs-lookup"><span data-stu-id="47836-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="47836-405">已修正的問題 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="47836-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="47836-406">CertificateInformation 為可設定的屬性，允許 Set-AzureRmApiManagement Cmdlet 正常運作。</span><span class="sxs-lookup"><span data-stu-id="47836-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="47836-407">已藉由升級至 4.0.4-preview NuGet 而修正</span><span class="sxs-lookup"><span data-stu-id="47836-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="47836-408">已修正的問題 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="47836-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="47836-409">已修正依產品名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="47836-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="47836-410">已修正的問題 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="47836-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="47836-411">已修正依 API 名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="47836-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="47836-412">已新增對 AzureMonitor 記錄器的支援</span><span class="sxs-lookup"><span data-stu-id="47836-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="47836-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-413">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-414">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="47836-415">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="47836-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="47836-416">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="47836-417">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="47836-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-418">AzureRM.Network</span></span>
* <span data-ttu-id="47836-419">已將預設的 Cmdlet 輸出表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="47836-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="47836-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="47836-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="47836-421">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="47836-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="47836-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-422">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-423">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47836-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47836-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47836-425">已修正的問題</span><span class="sxs-lookup"><span data-stu-id="47836-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47836-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47836-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47836-427">已新增對 MultiValue 路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="47836-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="47836-428">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="47836-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="47836-429">已新增對子網路路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="47836-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="47836-430">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="47836-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="47836-431">已新增對設定檔中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="47836-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="47836-432">已新增對設定檔中預期狀態碼的支援</span><span class="sxs-lookup"><span data-stu-id="47836-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="47836-433">已新增對端點中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="47836-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="47836-434">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="47836-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47836-435">一般</span><span class="sxs-lookup"><span data-stu-id="47836-435">General</span></span>
* <span data-ttu-id="47836-436">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="47836-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-437">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-438">已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖</span><span class="sxs-lookup"><span data-stu-id="47836-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-439">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-440">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="47836-441">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="47836-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="47836-442">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="47836-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="47836-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="47836-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="47836-444">修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-445">AzureRM.Network</span></span>
* <span data-ttu-id="47836-446">已將預設模式表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="47836-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="47836-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="47836-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="47836-448">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="47836-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-449">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-450">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47836-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47836-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47836-452">修正問題</span><span class="sxs-lookup"><span data-stu-id="47836-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47836-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47836-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47836-454">支援 MultiValue 路由方法</span><span class="sxs-lookup"><span data-stu-id="47836-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="47836-455">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="47836-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="47836-456">支援子網路路由方法</span><span class="sxs-lookup"><span data-stu-id="47836-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="47836-457">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="47836-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="47836-458">支援設定檔中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="47836-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="47836-459">支援設定檔中的預期狀態碼</span><span class="sxs-lookup"><span data-stu-id="47836-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="47836-460">支援端點中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="47836-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47836-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47836-461">AzureRM.Websites</span></span>
* <span data-ttu-id="47836-462">已修正未正確設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="47836-463">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="47836-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47836-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-464">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-465">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="47836-466">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="47836-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="47836-467">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="47836-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="47836-468">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="47836-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="47836-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-469">Azure.Storage</span></span>
* <span data-ttu-id="47836-470">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="47836-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="47836-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="47836-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="47836-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47836-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="47836-473">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="47836-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47836-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="47836-475">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47836-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47836-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47836-477">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="47836-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="47836-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="47836-479">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="47836-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="47836-480">AzureRM.Automation</span></span>
* <span data-ttu-id="47836-481">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="47836-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="47836-482">AzureRM.Backup</span></span>
* <span data-ttu-id="47836-483">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="47836-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="47836-484">AzureRM.Batch</span></span>
* <span data-ttu-id="47836-485">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="47836-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="47836-486">AzureRM.Billing</span></span>
* <span data-ttu-id="47836-487">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="47836-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="47836-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="47836-489">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="47836-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47836-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="47836-491">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-492">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-493">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="47836-494">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="47836-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="47836-495">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="47836-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="47836-496">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="47836-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="47836-497">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="47836-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="47836-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="47836-499">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="47836-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="47836-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="47836-501">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="47836-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="47836-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="47836-503">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="47836-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="47836-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="47836-505">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="47836-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47836-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="47836-507">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="47836-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="47836-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="47836-509">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47836-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47836-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47836-511">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="47836-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="47836-512">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="47836-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="47836-513">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="47836-514">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="47836-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="47836-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="47836-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="47836-516">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="47836-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="47836-517">AzureRM.Dns</span></span>
* <span data-ttu-id="47836-518">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="47836-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47836-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="47836-520">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="47836-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="47836-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="47836-522">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="47836-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47836-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="47836-524">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="47836-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="47836-525">AzureRM.Insights</span></span>
* <span data-ttu-id="47836-526">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="47836-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="47836-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="47836-528">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47836-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47836-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47836-530">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="47836-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47836-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="47836-532">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="47836-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="47836-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="47836-534">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="47836-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="47836-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="47836-536">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="47836-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="47836-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="47836-538">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="47836-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="47836-539">AzureRM.Media</span></span>
* <span data-ttu-id="47836-540">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-541">AzureRM.Network</span></span>
* <span data-ttu-id="47836-542">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="47836-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="47836-543">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="47836-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="47836-544">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="47836-545">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="47836-546">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="47836-547">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="47836-548">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="47836-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="47836-549">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="47836-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="47836-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="47836-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="47836-551">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="47836-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47836-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="47836-553">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="47836-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47836-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="47836-555">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="47836-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="47836-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="47836-557">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="47836-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47836-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="47836-559">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47836-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47836-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47836-561">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="47836-562">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="47836-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="47836-563">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="47836-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="47836-564">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="47836-565">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="47836-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="47836-566">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="47836-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="47836-567">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="47836-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="47836-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="47836-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="47836-569">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="47836-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47836-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="47836-571">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="47836-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="47836-572">AzureRM.Relay</span></span>
* <span data-ttu-id="47836-573">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-574">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-575">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="47836-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="47836-576">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="47836-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="47836-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47836-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="47836-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47836-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="47836-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47836-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="47836-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47836-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="47836-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="47836-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="47836-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="47836-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="47836-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="47836-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="47836-584">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="47836-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="47836-585">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="47836-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="47836-586">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="47836-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="47836-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="47836-588">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47836-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47836-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47836-590">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47836-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47836-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47836-592">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47836-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-593">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-594">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="47836-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-595">AzureRM.Storage</span></span>
* <span data-ttu-id="47836-596">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="47836-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="47836-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="47836-598">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="47836-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="47836-599">AzureRM.Tags</span></span>
* <span data-ttu-id="47836-600">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47836-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47836-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47836-602">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="47836-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="47836-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="47836-604">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47836-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47836-605">AzureRM.Websites</span></span>
* <span data-ttu-id="47836-606">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="47836-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="47836-607">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="47836-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47836-608">一般</span><span class="sxs-lookup"><span data-stu-id="47836-608">General</span></span>
* <span data-ttu-id="47836-609">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="47836-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="47836-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-610">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-611">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="47836-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="47836-612">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="47836-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-613">Azure.Storage</span></span>
* <span data-ttu-id="47836-614">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="47836-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="47836-615">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="47836-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47836-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47836-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47836-617">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="47836-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="47836-618">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="47836-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="47836-619">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="47836-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="47836-620">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="47836-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="47836-621">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="47836-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="47836-622">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="47836-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-623">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-624">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="47836-625">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="47836-626">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="47836-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="47836-627">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="47836-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="47836-628">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="47836-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="47836-629">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="47836-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="47836-630">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="47836-631">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="47836-632">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="47836-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="47836-633">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="47836-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="47836-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47836-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="47836-635">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="47836-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="47836-636">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="47836-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="47836-637">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="47836-638">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47836-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47836-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47836-640">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="47836-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="47836-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="47836-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="47836-642">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="47836-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="47836-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="47836-643">AzureRM.Insights</span></span>
* <span data-ttu-id="47836-644">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="47836-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="47836-645">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="47836-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47836-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47836-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47836-647">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="47836-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-648">AzureRM.Network</span></span>
* <span data-ttu-id="47836-649">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="47836-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-650">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-651">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="47836-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="47836-652">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="47836-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47836-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47836-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47836-654">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="47836-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="47836-655">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="47836-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="47836-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-656">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-657">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="47836-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="47836-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="47836-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="47836-659">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="47836-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="47836-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="47836-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="47836-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="47836-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="47836-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="47836-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="47836-663">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="47836-664">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="47836-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="47836-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-665">AzureRM.Storage</span></span>
* <span data-ttu-id="47836-666">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="47836-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="47836-667">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="47836-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="47836-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47836-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="47836-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47836-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="47836-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47836-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="47836-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="47836-671">AzureRM.Tags</span></span>
* <span data-ttu-id="47836-672">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="47836-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="47836-673">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="47836-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47836-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-674">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-675">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="47836-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="47836-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-676">Azure.Storage</span></span>
* <span data-ttu-id="47836-677">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="47836-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="47836-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="47836-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="47836-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="47836-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="47836-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47836-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="47836-681">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="47836-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="47836-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="47836-682">AzureRM.Automation</span></span>
* <span data-ttu-id="47836-683">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="47836-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-684">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-685">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47836-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="47836-686">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="47836-687">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="47836-688">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="47836-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="47836-689">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="47836-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="47836-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="47836-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="47836-691">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="47836-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47836-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47836-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47836-693">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="47836-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="47836-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47836-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="47836-695">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="47836-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-696">AzureRM.Network</span></span>
* <span data-ttu-id="47836-697">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="47836-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="47836-698">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="47836-699">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和 Zones 支援</span><span class="sxs-lookup"><span data-stu-id="47836-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="47836-700">New-AzureRmApplicationGatewaySku：已新增新的 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="47836-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="47836-701">Set-AzureRmApplicationGatewaySku：已新增新的 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="47836-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="47836-702">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="47836-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="47836-703">AzureRM.Relay</span></span>
* <span data-ttu-id="47836-704">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="47836-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-705">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-706">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="47836-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="47836-707">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="47836-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="47836-708">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="47836-709">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="47836-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="47836-710">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="47836-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="47836-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47836-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47836-712">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="47836-713">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="47836-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="47836-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="47836-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="47836-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="47836-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="47836-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="47836-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="47836-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="47836-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="47836-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="47836-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="47836-719">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="47836-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47836-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47836-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47836-721">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="47836-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47836-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-722">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-723">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="47836-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="47836-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="47836-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47836-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47836-726">AzureRM.Websites</span></span>
* <span data-ttu-id="47836-727">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="47836-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="47836-728">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="47836-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="47836-729">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="47836-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="47836-730">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="47836-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47836-731">一般</span><span class="sxs-lookup"><span data-stu-id="47836-731">General</span></span>
* <span data-ttu-id="47836-732">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="47836-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="47836-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-733">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-734">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="47836-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-735">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-736">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="47836-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="47836-737">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="47836-738">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="47836-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="47836-739">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="47836-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="47836-740">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47836-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="47836-741">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="47836-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="47836-742">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47836-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="47836-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="47836-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="47836-744">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="47836-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="47836-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="47836-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="47836-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="47836-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="47836-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="47836-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47836-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47836-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47836-749">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="47836-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="47836-750">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="47836-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="47836-751">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="47836-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="47836-752">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="47836-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="47836-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="47836-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="47836-754">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="47836-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="47836-755">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="47836-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="47836-756">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="47836-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="47836-757">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="47836-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47836-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47836-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47836-759">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="47836-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-760">AzureRM.Network</span></span>
* <span data-ttu-id="47836-761">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="47836-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="47836-762">已新增功能的新命令：透過 ARM 的 ExpressRoute 合作夥伴</span><span class="sxs-lookup"><span data-stu-id="47836-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="47836-763">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="47836-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="47836-764">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="47836-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="47836-765">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="47836-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="47836-766">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="47836-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="47836-767">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="47836-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="47836-768">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="47836-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="47836-769">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="47836-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="47836-770">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="47836-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47836-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47836-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47836-772">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="47836-773">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="47836-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="47836-774">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="47836-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-775">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-776">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="47836-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="47836-777">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="47836-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="47836-778">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="47836-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="47836-779">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="47836-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="47836-780">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="47836-781">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="47836-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="47836-782">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="47836-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="47836-783">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="47836-784">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="47836-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="47836-785">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="47836-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="47836-786">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="47836-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="47836-787">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="47836-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="47836-788">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="47836-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="47836-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47836-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="47836-790">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="47836-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47836-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-791">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-792">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="47836-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="47836-793">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="47836-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="47836-794">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="47836-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47836-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-795">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-796">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="47836-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="47836-797">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="47836-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="47836-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="47836-798">Azure.Storage</span></span>
* <span data-ttu-id="47836-799">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="47836-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-800">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-801">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="47836-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="47836-802">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="47836-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="47836-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="47836-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="47836-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="47836-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="47836-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="47836-806">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="47836-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="47836-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47836-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="47836-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47836-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="47836-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47836-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="47836-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="47836-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="47836-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="47836-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="47836-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47836-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="47836-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="47836-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="47836-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="47836-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="47836-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47836-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="47836-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47836-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="47836-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47836-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="47836-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47836-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="47836-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="47836-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="47836-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="47836-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="47836-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="47836-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="47836-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="47836-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="47836-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="47836-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="47836-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="47836-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="47836-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="47836-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="47836-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47836-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="47836-827">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="47836-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="47836-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47836-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47836-829">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="47836-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="47836-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47836-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="47836-831">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="47836-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="47836-832">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="47836-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="47836-833">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="47836-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="47836-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47836-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47836-835">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="47836-836">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47836-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47836-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-837">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-838">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="47836-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47836-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47836-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47836-840">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="47836-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47836-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47836-841">AzureRM.Websites</span></span>
* <span data-ttu-id="47836-842">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="47836-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="47836-843">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="47836-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="47836-844">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="47836-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="47836-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47836-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="47836-846">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="47836-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="47836-847">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="47836-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47836-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-848">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-849">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="47836-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="47836-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="47836-850">AzureRM.Compute</span></span>
* <span data-ttu-id="47836-851">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="47836-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="47836-852">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="47836-853">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="47836-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="47836-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47836-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="47836-855">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="47836-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="47836-856">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="47836-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="47836-857">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="47836-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="47836-858">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="47836-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="47836-859">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="47836-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="47836-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47836-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="47836-861">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="47836-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="47836-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-862">AzureRM.Network</span></span>
* <span data-ttu-id="47836-863">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="47836-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="47836-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="47836-864">AzureRM.Resources</span></span>
* <span data-ttu-id="47836-865">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="47836-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="47836-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="47836-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="47836-867">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="47836-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="47836-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-868">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-869">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="47836-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="47836-870">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47836-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="47836-871">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47836-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="47836-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47836-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="47836-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="47836-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="47836-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47836-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="47836-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="47836-875">AzureRM.Websites</span></span>
* <span data-ttu-id="47836-876">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="47836-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="47836-877">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="47836-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="47836-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="47836-878">AzureRM.Profile</span></span>
* <span data-ttu-id="47836-879">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="47836-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="47836-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47836-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="47836-881">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="47836-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="47836-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47836-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="47836-883">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="47836-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="47836-884">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="47836-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="47836-885">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="47836-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="47836-886">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="47836-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="47836-887">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="47836-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="47836-888">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="47836-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="47836-889">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="47836-889">Added support for MSI identity</span></span>
* <span data-ttu-id="47836-890">已新增透過URL 接受原則的支援注意：下列 Cmdlet 將於未來版本中加以取代</span><span class="sxs-lookup"><span data-stu-id="47836-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="47836-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="47836-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="47836-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="47836-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="47836-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="47836-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="47836-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="47836-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="47836-895">AzureRM.Batch</span></span>
* <span data-ttu-id="47836-896">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="47836-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="47836-897">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="47836-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="47836-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="47836-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="47836-899">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="47836-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="47836-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47836-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="47836-901">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="47836-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="47836-902">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="47836-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="47836-903">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="47836-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="47836-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="47836-904">AzureRM.Network</span></span>
* <span data-ttu-id="47836-905">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="47836-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="47836-906">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="47836-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="47836-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="47836-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="47836-908">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="47836-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="47836-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="47836-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="47836-910">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="47836-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="47836-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="47836-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="47836-912">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="47836-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="47836-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="47836-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="47836-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47836-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="47836-915">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="47836-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="47836-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="47836-916">AzureRM.Sql</span></span>
* <span data-ttu-id="47836-917">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="47836-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="47836-918">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="47836-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="47836-919">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="47836-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="47836-920">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="47836-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="47836-921">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="47836-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="47836-922">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47836-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="47836-923">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="47836-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="47836-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="47836-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="47836-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="47836-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="47836-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="47836-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="47836-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47836-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="47836-928">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="47836-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
