---
ms.openlocfilehash: 9915ff37e59a73c1d226a216213fd9016b55d3d4
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882201"
---
## <a name="150---march-2019"></a><span data-ttu-id="eeb0f-101">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-101">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eeb0f-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eeb0f-102">Az.Accounts</span></span>
* <span data-ttu-id="eeb0f-103">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-103">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="eeb0f-104">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-104">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eeb0f-105">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eeb0f-105">Az.Automation</span></span>
* <span data-ttu-id="eeb0f-106">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-106">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="eeb0f-107">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-107">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="eeb0f-108">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="eeb0f-108">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="eeb0f-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eeb0f-109">Az.Cdn</span></span>
* <span data-ttu-id="eeb0f-110">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-110">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eeb0f-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-111">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-112">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-112">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eeb0f-113">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eeb0f-113">Az.DataFactory</span></span>
* <span data-ttu-id="eeb0f-114">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="eeb0f-114">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eeb0f-115">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eeb0f-115">Az.LogicApp</span></span>
* <span data-ttu-id="eeb0f-116">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="eeb0f-116">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eeb0f-117">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eeb0f-117">Az.Network</span></span>
* <span data-ttu-id="eeb0f-118">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-118">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eeb0f-119">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-119">Az.RecoveryServices</span></span>
* <span data-ttu-id="eeb0f-120">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-120">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="eeb0f-121">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="eeb0f-121">SDK Update</span></span>
* <span data-ttu-id="eeb0f-122">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="eeb0f-122">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="eeb0f-123">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="eeb0f-123">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="eeb0f-124">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-124">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-125">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-125">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="eeb0f-126">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="eeb0f-126">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="eeb0f-127">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-127">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="eeb0f-128">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="eeb0f-128">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="eeb0f-129">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-129">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="eeb0f-130">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="eeb0f-130">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="eeb0f-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-131">Az.Sql</span></span>
* <span data-ttu-id="eeb0f-132">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-132">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="eeb0f-133">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-133">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eeb0f-134">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb0f-134">Az.Storage</span></span>
* <span data-ttu-id="eeb0f-135">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eeb0f-135">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="eeb0f-136">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-136">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="eeb0f-137">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-137">Az.AnalysisServices</span></span>
* <span data-ttu-id="eeb0f-138">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-138">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eeb0f-139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eeb0f-139">Az.Automation</span></span>
* <span data-ttu-id="eeb0f-140">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="eeb0f-140">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="eeb0f-141">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-141">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="eeb0f-142">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="eeb0f-142">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="eeb0f-143">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-143">Az.CognitiveServices</span></span>
* <span data-ttu-id="eeb0f-144">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-144">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eeb0f-145">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-145">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-146">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-146">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="eeb0f-147">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="eeb0f-147">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="eeb0f-148">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-148">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="eeb0f-149">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-149">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eeb0f-150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb0f-150">Az.DataLakeStore</span></span>
* <span data-ttu-id="eeb0f-151">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-151">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="eeb0f-152">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="eeb0f-152">Az.EventHub</span></span>
* <span data-ttu-id="eeb0f-153">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="eeb0f-153">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="eeb0f-154">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb0f-154">Az.KeyVault</span></span>
* <span data-ttu-id="eeb0f-155">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="eeb0f-155">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eeb0f-156">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eeb0f-156">Az.LogicApp</span></span>
* <span data-ttu-id="eeb0f-157">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="eeb0f-157">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="eeb0f-158">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="eeb0f-158">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="eeb0f-159">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-159">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="eeb0f-160">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eeb0f-160">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eeb0f-161">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eeb0f-161">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eeb0f-162">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eeb0f-162">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="eeb0f-163">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="eeb0f-163">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="eeb0f-164">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-164">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="eeb0f-165">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb0f-165">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eeb0f-166">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb0f-166">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eeb0f-167">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb0f-167">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="eeb0f-168">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb0f-168">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="eeb0f-169">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="eeb0f-169">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="eeb0f-170">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eeb0f-170">Az.Monitor</span></span>
* <span data-ttu-id="eeb0f-171">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="eeb0f-171">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eeb0f-172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eeb0f-172">Az.Network</span></span>
* <span data-ttu-id="eeb0f-173">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-173">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="eeb0f-174">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eeb0f-174">Az.OperationalInsights</span></span>
* <span data-ttu-id="eeb0f-175">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-175">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="eeb0f-176">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-176">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="eeb0f-177">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-177">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="eeb0f-178">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-178">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-179">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-179">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="eeb0f-180">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-180">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="eeb0f-181">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-181">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="eeb0f-182">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="eeb0f-182">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="eeb0f-183">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-183">Az.Sql</span></span>
* <span data-ttu-id="eeb0f-184">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-184">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="eeb0f-185">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="eeb0f-185">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eeb0f-186">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb0f-186">Az.Websites</span></span>
* <span data-ttu-id="eeb0f-187">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-187">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="eeb0f-188">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-188">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eeb0f-189">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eeb0f-189">Az.Accounts</span></span>
* <span data-ttu-id="eeb0f-190">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eeb0f-190">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="eeb0f-191">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-191">Az.AnalysisServices</span></span>
<span data-ttu-id="eeb0f-192">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-192">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eeb0f-193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-193">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-194">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-194">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="eeb0f-195">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="eeb0f-195">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="eeb0f-196">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-196">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eeb0f-197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-197">Az.RecoveryServices</span></span>
<span data-ttu-id="eeb0f-198">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-198">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="eeb0f-199">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-199">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-200">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="eeb0f-200">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="eeb0f-201">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="eeb0f-201">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="eeb0f-202">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-202">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="eeb0f-203">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="eeb0f-203">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="eeb0f-204">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-204">Az.Sql</span></span>
* <span data-ttu-id="eeb0f-205">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb0f-205">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="eeb0f-206">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-206">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="eeb0f-207">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="eeb0f-207">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="eeb0f-208">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-208">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eeb0f-209">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eeb0f-209">Az.Accounts</span></span>
* <span data-ttu-id="eeb0f-210">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="eeb0f-210">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="eeb0f-211">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-211">Az.AnalysisServices</span></span>
* <span data-ttu-id="eeb0f-212">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="eeb0f-212">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="eeb0f-213">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-213">Az.RecoveryServices</span></span>
* <span data-ttu-id="eeb0f-214">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="eeb0f-214">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="eeb0f-215">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-215">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eeb0f-216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eeb0f-216">Az.Accounts</span></span>
* <span data-ttu-id="eeb0f-217">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="eeb0f-217">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="eeb0f-218">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-218">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eeb0f-219">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="eeb0f-219">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="eeb0f-220">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="eeb0f-220">Az.Aks</span></span>
* <span data-ttu-id="eeb0f-221">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-221">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="eeb0f-222">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eeb0f-222">Az.Automation</span></span>
* <span data-ttu-id="eeb0f-223">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-223">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="eeb0f-224">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-224">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="eeb0f-225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="eeb0f-225">Az.Cdn</span></span>
* <span data-ttu-id="eeb0f-226">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-226">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eeb0f-227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-227">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-228">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-228">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="eeb0f-229">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eeb0f-229">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="eeb0f-230">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="eeb0f-230">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="eeb0f-231">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eeb0f-231">Az.ContainerRegistry</span></span>
* <span data-ttu-id="eeb0f-232">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-232">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="eeb0f-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="eeb0f-233">Az.DataFactory</span></span>
* <span data-ttu-id="eeb0f-234">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="eeb0f-234">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eeb0f-235">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb0f-235">Az.DataLakeStore</span></span>
* <span data-ttu-id="eeb0f-236">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-236">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="eeb0f-237">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="eeb0f-237">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="eeb0f-238">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-238">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eeb0f-239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eeb0f-239">Az.IotHub</span></span>
* <span data-ttu-id="eeb0f-240">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-240">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="eeb0f-241">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb0f-241">Az.KeyVault</span></span>
* <span data-ttu-id="eeb0f-242">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-242">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eeb0f-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eeb0f-243">Az.Network</span></span>
* <span data-ttu-id="eeb0f-244">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-244">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="eeb0f-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-245">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-246">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-246">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="eeb0f-247">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-247">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="eeb0f-248">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="eeb0f-248">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="eeb0f-249">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-249">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="eeb0f-250">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-250">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="eeb0f-251">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-251">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="eeb0f-252">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="eeb0f-252">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eeb0f-253">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb0f-253">Az.ServiceFabric</span></span>
* <span data-ttu-id="eeb0f-254">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="eeb0f-254">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="eeb0f-255">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-255">Fix some error messages.</span></span>
* <span data-ttu-id="eeb0f-256">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-256">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="eeb0f-257">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-257">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="eeb0f-258">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="eeb0f-258">Az.SignalR</span></span>
* <span data-ttu-id="eeb0f-259">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-259">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="eeb0f-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-260">Az.Sql</span></span>
* <span data-ttu-id="eeb0f-261">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-261">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eeb0f-262">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="eeb0f-262">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="eeb0f-263">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-263">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="eeb0f-264">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="eeb0f-264">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eeb0f-265">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb0f-265">Az.Storage</span></span>
* <span data-ttu-id="eeb0f-266">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-266">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eeb0f-267">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-267">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="eeb0f-268">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="eeb0f-268">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="eeb0f-269">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="eeb0f-269">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="eeb0f-270">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="eeb0f-270">Az.TrafficManager</span></span>
* <span data-ttu-id="eeb0f-271">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-271">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eeb0f-272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb0f-272">Az.Websites</span></span>
* <span data-ttu-id="eeb0f-273">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-273">Update incorrect online help URLs</span></span>
* <span data-ttu-id="eeb0f-274">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-274">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="eeb0f-275">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="eeb0f-275">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="eeb0f-276">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-276">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="eeb0f-277">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eeb0f-277">Az.Accounts</span></span>
* <span data-ttu-id="eeb0f-278">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="eeb0f-278">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eeb0f-279">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-279">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-280">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="eeb0f-280">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="eeb0f-281">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="eeb0f-281">Updated the description of ID in help files</span></span>
* <span data-ttu-id="eeb0f-282">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-282">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eeb0f-283">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb0f-283">Az.DataLakeStore</span></span>
* <span data-ttu-id="eeb0f-284">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-284">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="eeb0f-285">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="eeb0f-285">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="eeb0f-286">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="eeb0f-286">Az.EventGrid</span></span>
* <span data-ttu-id="eeb0f-287">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-287">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="eeb0f-288">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-288">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="eeb0f-289">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="eeb0f-289">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="eeb0f-290">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="eeb0f-290">Event Time-To-Live,</span></span>
        - <span data-ttu-id="eeb0f-291">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="eeb0f-291">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="eeb0f-292">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-292">Dead letter endpoint.</span></span>
    - <span data-ttu-id="eeb0f-293">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="eeb0f-293">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="eeb0f-294">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="eeb0f-294">Event Time-To-Live,</span></span>
        - <span data-ttu-id="eeb0f-295">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="eeb0f-295">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="eeb0f-296">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-296">Dead letter endpoint.</span></span>
* <span data-ttu-id="eeb0f-297">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-297">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="eeb0f-298">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-298">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="eeb0f-299">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="eeb0f-299">Az.IotHub</span></span>
* <span data-ttu-id="eeb0f-300">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="eeb0f-300">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="eeb0f-301">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="eeb0f-301">Az.LogicApp</span></span>
* <span data-ttu-id="eeb0f-302">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="eeb0f-302">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="eeb0f-303">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-303">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-304">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-304">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="eeb0f-305">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="eeb0f-305">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="eeb0f-306">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="eeb0f-306">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="eeb0f-307">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="eeb0f-307">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="eeb0f-308">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="eeb0f-308">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="eeb0f-309">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="eeb0f-309">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="eeb0f-310">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="eeb0f-310">Az.SignalR</span></span>
* <span data-ttu-id="eeb0f-311">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-311">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="eeb0f-312">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-312">Az.Sql</span></span>
* <span data-ttu-id="eeb0f-313">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-313">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="eeb0f-314">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb0f-314">Az.Storage</span></span>
* <span data-ttu-id="eeb0f-315">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="eeb0f-315">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="eeb0f-316">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="eeb0f-316">New-AzStorageContext</span></span>
* <span data-ttu-id="eeb0f-317">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="eeb0f-317">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="eeb0f-318">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="eeb0f-318">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eeb0f-319">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb0f-319">Az.Websites</span></span>
* <span data-ttu-id="eeb0f-320">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="eeb0f-320">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="eeb0f-321">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-321">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="eeb0f-322">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-322">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="eeb0f-323">一般</span><span class="sxs-lookup"><span data-stu-id="eeb0f-323">General</span></span>

- <span data-ttu-id="eeb0f-324">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="eeb0f-324">General Availability of Az Module</span></span>
- <span data-ttu-id="eeb0f-325">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="eeb0f-325">Online help for each module</span></span>
- <span data-ttu-id="eeb0f-326">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-326">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="eeb0f-327">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-327">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="eeb0f-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eeb0f-328">Az.Accounts</span></span>
- <span data-ttu-id="eeb0f-329">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="eeb0f-329">Changed from Az.Profile</span></span>
- <span data-ttu-id="eeb0f-330">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="eeb0f-330">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="eeb0f-331">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eeb0f-331">Az.ApiManagement</span></span>
- <span data-ttu-id="eeb0f-332">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="eeb0f-332">Fixes for #7002</span></span>
- <span data-ttu-id="eeb0f-333">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="eeb0f-334">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="eeb0f-334">Az.Batch</span></span>
- <span data-ttu-id="eeb0f-335">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-335">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="eeb0f-336">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-336">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="eeb0f-337">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="eeb0f-338">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="eeb0f-338">Az.Billing</span></span>
- <span data-ttu-id="eeb0f-339">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-339">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="eeb0f-340">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-340">Az.CognitivServices</span></span>
- <span data-ttu-id="eeb0f-341">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="eeb0f-341">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="eeb0f-342">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="eeb0f-342">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="eeb0f-343">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eeb0f-343">Az.ContainerInstance</span></span>
- <span data-ttu-id="eeb0f-344">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-344">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="eeb0f-345">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="eeb0f-345">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="eeb0f-346">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-346">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="eeb0f-347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb0f-347">Az.DataLakeStore</span></span>
- <span data-ttu-id="eeb0f-348">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-348">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="eeb0f-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="eeb0f-349">Az.Monitor</span></span>
- <span data-ttu-id="eeb0f-350">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-350">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="eeb0f-351">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="eeb0f-351">Az.KeyVault</span></span>
- <span data-ttu-id="eeb0f-352">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="eeb0f-352">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="eeb0f-353">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="eeb0f-353">Az.MachineLearning</span></span>
- <span data-ttu-id="eeb0f-354">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-354">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="eeb0f-355">Az.Media</span><span class="sxs-lookup"><span data-stu-id="eeb0f-355">Az.Media</span></span>
- <span data-ttu-id="eeb0f-356">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="eeb0f-356">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="eeb0f-357">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eeb0f-357">Az.Network</span></span>
<span data-ttu-id="eeb0f-358">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-358">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="eeb0f-359">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="eeb0f-359">New cmdlets added:</span></span>
        - <span data-ttu-id="eeb0f-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-360">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eeb0f-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-361">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eeb0f-362">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-362">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eeb0f-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-363">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eeb0f-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-364">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="eeb0f-365">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="eeb0f-365">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="eeb0f-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-366">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="eeb0f-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeb0f-367">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="eeb0f-368">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-368">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="eeb0f-369">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eeb0f-369">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="eeb0f-370">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eeb0f-370">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="eeb0f-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eeb0f-371">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="eeb0f-372">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="eeb0f-372">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="eeb0f-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="eeb0f-373">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="eeb0f-374">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-374">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="eeb0f-375">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-375">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="eeb0f-376">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb0f-376">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="eeb0f-377">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb0f-377">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="eeb0f-378">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="eeb0f-378">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="eeb0f-379">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-379">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="eeb0f-380">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-380">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="eeb0f-381">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="eeb0f-381">Az.OperationalInsights</span></span>
- <span data-ttu-id="eeb0f-382">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-382">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="eeb0f-383">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb0f-383">Az.Profile</span></span>
- <span data-ttu-id="eeb0f-384">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="eeb0f-384">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="eeb0f-385">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-385">Az.RecoveryServices</span></span>
- <span data-ttu-id="eeb0f-386">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="eeb0f-387">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-387">Az.Resources</span></span>
- <span data-ttu-id="eeb0f-388">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="eeb0f-389">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb0f-389">Az.ServiceFabric</span></span>
- <span data-ttu-id="eeb0f-390">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="eeb0f-390">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="eeb0f-391">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-391">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="eeb0f-392">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="eeb0f-392">Az.SIgnalR</span></span>
- <span data-ttu-id="eeb0f-393">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="eeb0f-393">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="eeb0f-394">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-394">Az.Sql</span></span>
- <span data-ttu-id="eeb0f-395">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="eeb0f-395">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="eeb0f-396">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-396">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="eeb0f-397">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-397">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="eeb0f-398">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb0f-398">Az.Storage</span></span>
- <span data-ttu-id="eeb0f-399">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-399">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="eeb0f-400">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb0f-400">Az.Websites</span></span>
- <span data-ttu-id="eeb0f-401">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-401">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="eeb0f-402">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-402">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="eeb0f-403">一般</span><span class="sxs-lookup"><span data-stu-id="eeb0f-403">General</span></span>

* <span data-ttu-id="eeb0f-404">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="eeb0f-404">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="eeb0f-405">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-405">Az.Compute</span></span>

* <span data-ttu-id="eeb0f-406">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-406">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="eeb0f-407">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb0f-407">Az.DataLakeStore</span></span>

* <span data-ttu-id="eeb0f-408">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="eeb0f-408">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="eeb0f-409">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="eeb0f-409">Az.FrontDoor</span></span>

* <span data-ttu-id="eeb0f-410">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="eeb0f-410">Fixed some broken links</span></span>
    - <span data-ttu-id="eeb0f-411">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-411">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="eeb0f-412">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-412">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="eeb0f-413">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-413">Az.RecoveryServices</span></span>

* <span data-ttu-id="eeb0f-414">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-414">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="eeb0f-415">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-415">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="eeb0f-416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-416">Az.Resources</span></span>

* <span data-ttu-id="eeb0f-417">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="eeb0f-417">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="eeb0f-418">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-418">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="eeb0f-419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-419">Az.Sql</span></span>

* <span data-ttu-id="eeb0f-420">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="eeb0f-420">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="eeb0f-421">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-421">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="eeb0f-422">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-422">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="eeb0f-423">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb0f-423">Az.Storage</span></span>

* <span data-ttu-id="eeb0f-424">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="eeb0f-424">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="eeb0f-425">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="eeb0f-425">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="eeb0f-426">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eeb0f-426">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="eeb0f-427">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="eeb0f-427">Support Static Website configuration</span></span>
    - <span data-ttu-id="eeb0f-428">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="eeb0f-428">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="eeb0f-429">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="eeb0f-429">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="eeb0f-430">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb0f-430">Az.Websites</span></span>

* <span data-ttu-id="eeb0f-431">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="eeb0f-431">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="eeb0f-432">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-432">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="eeb0f-433">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-433">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="eeb0f-434">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-434">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="eeb0f-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eeb0f-435">Az.ApiManagement</span></span>
* <span data-ttu-id="eeb0f-436">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="eeb0f-436">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="eeb0f-437">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="eeb0f-437">Az.Automation</span></span>
* <span data-ttu-id="eeb0f-438">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-438">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="eeb0f-439">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-439">Added Update Management cmdlets</span></span>
* <span data-ttu-id="eeb0f-440">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-440">Added Source Control cmdlets</span></span>
* <span data-ttu-id="eeb0f-441">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-441">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="eeb0f-442">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="eeb0f-442">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="eeb0f-443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-443">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-444">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-444">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="eeb0f-445">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="eeb0f-445">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="eeb0f-446">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eeb0f-446">Az.ContainerInstance</span></span>
* <span data-ttu-id="eeb0f-447">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="eeb0f-447">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="eeb0f-448">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="eeb0f-448">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="eeb0f-449">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="eeb0f-449">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="eeb0f-450">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eeb0f-450">Az.Network</span></span>
* <span data-ttu-id="eeb0f-451">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="eeb0f-451">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="eeb0f-452">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="eeb0f-452">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="eeb0f-453">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-453">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="eeb0f-454">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-454">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="eeb0f-455">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="eeb0f-455">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="eeb0f-456">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-456">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="eeb0f-457">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-457">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="eeb0f-458">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="eeb0f-458">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="eeb0f-459">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-459">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="eeb0f-460">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="eeb0f-460">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="eeb0f-461">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="eeb0f-461">Az.Relay</span></span>
* <span data-ttu-id="eeb0f-462">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-462">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="eeb0f-463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-463">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-464">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="eeb0f-464">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="eeb0f-465">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="eeb0f-465">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="eeb0f-466">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="eeb0f-466">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="eeb0f-467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb0f-467">Az.ServiceFabric</span></span>
* <span data-ttu-id="eeb0f-468">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="eeb0f-468">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="eeb0f-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-469">Az.Sql</span></span>
* <span data-ttu-id="eeb0f-470">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-470">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="eeb0f-471">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eeb0f-471">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eeb0f-472">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eeb0f-472">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eeb0f-473">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eeb0f-473">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eeb0f-474">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eeb0f-474">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="eeb0f-475">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb0f-475">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eeb0f-476">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb0f-476">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eeb0f-477">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb0f-477">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="eeb0f-478">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="eeb0f-478">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="eeb0f-479">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-479">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="eeb0f-480">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-480">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="eeb0f-481">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-481">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="eeb0f-482">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-482">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="eeb0f-483">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-483">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="eeb0f-484">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-484">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="eeb0f-485">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-485">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="eeb0f-486">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-486">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="eeb0f-487">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-487">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="eeb0f-488">一般</span><span class="sxs-lookup"><span data-stu-id="eeb0f-488">General</span></span>
* <span data-ttu-id="eeb0f-489">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="eeb0f-489">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="eeb0f-490">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb0f-490">Az.Profile</span></span>
* <span data-ttu-id="eeb0f-491">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eeb0f-491">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="eeb0f-492">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="eeb0f-492">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="eeb0f-493">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="eeb0f-493">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="eeb0f-494">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="eeb0f-494">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="eeb0f-495">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-495">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="eeb0f-496">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-496">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="eeb0f-497">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-497">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="eeb0f-498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-498">Az.CognitiveServices</span></span>
* <span data-ttu-id="eeb0f-499">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-499">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eeb0f-500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-500">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-501">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-501">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="eeb0f-502">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="eeb0f-502">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="eeb0f-503">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-503">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eeb0f-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb0f-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="eeb0f-505">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-505">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="eeb0f-506">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-506">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="eeb0f-507">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="eeb0f-507">Az.Insights</span></span>
* <span data-ttu-id="eeb0f-508">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="eeb0f-508">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="eeb0f-509">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-509">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="eeb0f-510">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="eeb0f-510">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="eeb0f-511">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="eeb0f-511">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eeb0f-512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eeb0f-512">Az.Network</span></span>
* <span data-ttu-id="eeb0f-513">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="eeb0f-513">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="eeb0f-514">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="eeb0f-514">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="eeb0f-515">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="eeb0f-515">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="eeb0f-516">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eeb0f-516">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="eeb0f-517">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="eeb0f-517">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="eeb0f-518">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="eeb0f-518">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="eeb0f-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="eeb0f-519">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="eeb0f-520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="eeb0f-520">Az.PolicyInsights</span></span>
* <span data-ttu-id="eeb0f-521">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-521">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="eeb0f-522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-522">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-523">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="eeb0f-523">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="eeb0f-524">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="eeb0f-524">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="eeb0f-525">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="eeb0f-525">Az.ServiceBus</span></span>
* <span data-ttu-id="eeb0f-526">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-526">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="eeb0f-527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="eeb0f-527">Az.ServiceFabric</span></span>
* <span data-ttu-id="eeb0f-528">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-528">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="eeb0f-529">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="eeb0f-529">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="eeb0f-530">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-530">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="eeb0f-531">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-531">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="eeb0f-532">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-532">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="eeb0f-533">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-533">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="eeb0f-534">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="eeb0f-534">Az.Profile</span></span>
* <span data-ttu-id="eeb0f-535">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-535">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="eeb0f-536">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="eeb0f-536">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eeb0f-537">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-537">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-538">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="eeb0f-538">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="eeb0f-539">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-539">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="eeb0f-540">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="eeb0f-540">Az.DataLakeStore</span></span>
* <span data-ttu-id="eeb0f-541">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="eeb0f-541">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="eeb0f-542">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-542">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="eeb0f-543">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-543">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="eeb0f-544">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-544">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="eeb0f-545">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-545">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eeb0f-546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eeb0f-546">Az.Network</span></span>
* <span data-ttu-id="eeb0f-547">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-547">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="eeb0f-548">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-548">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="eeb0f-549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-549">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-550">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-550">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="eeb0f-551">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-551">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="eeb0f-552">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-552">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="eeb0f-553">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="eeb0f-553">Azure.Storage</span></span>
* <span data-ttu-id="eeb0f-554">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-554">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="eeb0f-555">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="eeb0f-555">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="eeb0f-556">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eeb0f-556">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="eeb0f-557">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-557">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="eeb0f-558">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="eeb0f-558">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="eeb0f-559">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="eeb0f-559">Az.CognitiveServices</span></span>
* <span data-ttu-id="eeb0f-560">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-560">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="eeb0f-561">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="eeb0f-561">Az.Compute</span></span>
* <span data-ttu-id="eeb0f-562">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="eeb0f-562">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="eeb0f-563">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-563">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="eeb0f-564">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="eeb0f-564">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="eeb0f-565">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eeb0f-565">Az.DataFactoryV2</span></span>
* <span data-ttu-id="eeb0f-566">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-566">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="eeb0f-567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="eeb0f-567">Az.Network</span></span>
* <span data-ttu-id="eeb0f-568">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-568">Added NetworkProfile functionality.</span></span> <span data-ttu-id="eeb0f-569">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-569">new cmdlets added</span></span>
    - <span data-ttu-id="eeb0f-570">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eeb0f-570">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="eeb0f-571">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eeb0f-571">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="eeb0f-572">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eeb0f-572">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="eeb0f-573">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="eeb0f-573">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="eeb0f-574">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="eeb0f-574">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="eeb0f-575">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="eeb0f-575">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="eeb0f-576">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="eeb0f-576">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="eeb0f-577">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-577">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="eeb0f-578">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eeb0f-578">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="eeb0f-579">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="eeb0f-579">Az.RedisCache</span></span>
* <span data-ttu-id="eeb0f-580">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="eeb0f-580">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="eeb0f-581">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="eeb0f-581">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="eeb0f-582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="eeb0f-582">Az.Resources</span></span>
* <span data-ttu-id="eeb0f-583">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="eeb0f-583">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="eeb0f-584">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="eeb0f-584">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="eeb0f-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="eeb0f-585">Az.Sql</span></span>
* <span data-ttu-id="eeb0f-586">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="eeb0f-586">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="eeb0f-587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="eeb0f-587">Az.Websites</span></span>
* <span data-ttu-id="eeb0f-588">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="eeb0f-588">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="eeb0f-589">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="eeb0f-589">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="eeb0f-590">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="eeb0f-590">0.2.0 - September 2018</span></span>
 <span data-ttu-id="eeb0f-591">初始版本</span><span class="sxs-lookup"><span data-stu-id="eeb0f-591">Initial Release</span></span>