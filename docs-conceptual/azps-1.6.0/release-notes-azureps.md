---
ms.openlocfilehash: 2db9810e20254373a487013de50d4297d4ec50d5
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475189"
---
## <a name="160---march-2019"></a><span data-ttu-id="82f73-101">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="82f73-101">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="82f73-102">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="82f73-102">Highlights since the last major release</span></span>
* <span data-ttu-id="82f73-103">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="82f73-103">General availability of `Az` module</span></span>
* <span data-ttu-id="82f73-104">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="82f73-104">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="82f73-105">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="82f73-105">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="82f73-106">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="82f73-106">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="82f73-107">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="82f73-107">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="82f73-108">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="82f73-108">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="82f73-109">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-109">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82f73-110">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82f73-110">Az.Automation</span></span>
* <span data-ttu-id="82f73-111">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="82f73-111">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="82f73-112">動態分組</span><span class="sxs-lookup"><span data-stu-id="82f73-112">Dynamic grouping</span></span>
    * <span data-ttu-id="82f73-113">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="82f73-113">Pre-Post script</span></span>
    * <span data-ttu-id="82f73-114">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="82f73-114">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-115">Az.Compute</span></span>
* <span data-ttu-id="82f73-116">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-116">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="82f73-117">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="82f73-117">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82f73-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82f73-118">Az.KeyVault</span></span>
* <span data-ttu-id="82f73-119">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="82f73-119">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82f73-120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-120">Az.Network</span></span>
* <span data-ttu-id="82f73-121">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="82f73-121">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="82f73-122">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="82f73-122">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82f73-123">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82f73-123">Az.RecoveryServices</span></span>
* <span data-ttu-id="82f73-124">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="82f73-124">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="82f73-125">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="82f73-125">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="82f73-126">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-126">Az.Resources</span></span>
* <span data-ttu-id="82f73-127">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="82f73-127">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="82f73-128">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="82f73-128">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="82f73-129">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-129">Az.Sql</span></span>
* <span data-ttu-id="82f73-130">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="82f73-130">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82f73-131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82f73-131">Az.Storage</span></span>
* <span data-ttu-id="82f73-132">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="82f73-132">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="82f73-133">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="82f73-133">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="82f73-134">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="82f73-134">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="82f73-135">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="82f73-135">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="82f73-136">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="82f73-136">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="82f73-137">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="82f73-137">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="82f73-138">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="82f73-138">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82f73-139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82f73-139">Az.Websites</span></span>
* <span data-ttu-id="82f73-140">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="82f73-140">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="82f73-141">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="82f73-141">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82f73-142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82f73-142">Az.Accounts</span></span>
* <span data-ttu-id="82f73-143">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-143">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="82f73-144">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="82f73-144">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82f73-145">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82f73-145">Az.Automation</span></span>
* <span data-ttu-id="82f73-146">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-146">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="82f73-147">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="82f73-147">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="82f73-148">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="82f73-148">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82f73-149">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82f73-149">Az.Cdn</span></span>
* <span data-ttu-id="82f73-150">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-150">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-151">Az.Compute</span></span>
* <span data-ttu-id="82f73-152">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="82f73-152">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82f73-153">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82f73-153">Az.DataFactory</span></span>
* <span data-ttu-id="82f73-154">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="82f73-154">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82f73-155">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82f73-155">Az.LogicApp</span></span>
* <span data-ttu-id="82f73-156">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="82f73-156">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82f73-157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-157">Az.Network</span></span>
* <span data-ttu-id="82f73-158">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="82f73-158">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82f73-159">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82f73-159">Az.RecoveryServices</span></span>
* <span data-ttu-id="82f73-160">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="82f73-160">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="82f73-161">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="82f73-161">SDK Update</span></span>
* <span data-ttu-id="82f73-162">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="82f73-162">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="82f73-163">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="82f73-163">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="82f73-164">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-164">Az.Resources</span></span>
* <span data-ttu-id="82f73-165">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-165">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="82f73-166">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="82f73-166">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="82f73-167">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-167">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="82f73-168">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="82f73-168">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="82f73-169">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-169">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="82f73-170">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="82f73-170">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="82f73-171">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-171">Az.Sql</span></span>
* <span data-ttu-id="82f73-172">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="82f73-172">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="82f73-173">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="82f73-173">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82f73-174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82f73-174">Az.Storage</span></span>
* <span data-ttu-id="82f73-175">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82f73-175">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="82f73-176">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="82f73-176">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="82f73-177">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82f73-177">Az.AnalysisServices</span></span>
* <span data-ttu-id="82f73-178">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-178">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82f73-179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82f73-179">Az.Automation</span></span>
* <span data-ttu-id="82f73-180">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="82f73-180">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="82f73-181">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-181">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="82f73-182">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="82f73-182">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="82f73-183">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82f73-183">Az.CognitiveServices</span></span>
* <span data-ttu-id="82f73-184">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="82f73-184">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-185">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-185">Az.Compute</span></span>
* <span data-ttu-id="82f73-186">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="82f73-186">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="82f73-187">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="82f73-187">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="82f73-188">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-188">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="82f73-189">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="82f73-189">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82f73-190">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82f73-190">Az.DataLakeStore</span></span>
* <span data-ttu-id="82f73-191">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-191">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="82f73-192">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="82f73-192">Az.EventHub</span></span>
* <span data-ttu-id="82f73-193">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="82f73-193">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="82f73-194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82f73-194">Az.KeyVault</span></span>
* <span data-ttu-id="82f73-195">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="82f73-195">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82f73-196">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82f73-196">Az.LogicApp</span></span>
* <span data-ttu-id="82f73-197">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="82f73-197">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="82f73-198">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="82f73-198">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="82f73-199">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-199">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="82f73-200">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="82f73-200">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82f73-201">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="82f73-201">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82f73-202">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="82f73-202">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="82f73-203">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="82f73-203">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="82f73-204">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-204">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="82f73-205">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="82f73-205">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82f73-206">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="82f73-206">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82f73-207">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="82f73-207">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="82f73-208">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="82f73-208">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="82f73-209">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="82f73-209">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="82f73-210">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82f73-210">Az.Monitor</span></span>
* <span data-ttu-id="82f73-211">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="82f73-211">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82f73-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-212">Az.Network</span></span>
* <span data-ttu-id="82f73-213">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="82f73-213">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="82f73-214">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82f73-214">Az.OperationalInsights</span></span>
* <span data-ttu-id="82f73-215">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="82f73-215">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="82f73-216">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="82f73-216">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="82f73-217">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="82f73-217">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="82f73-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-218">Az.Resources</span></span>
* <span data-ttu-id="82f73-219">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-219">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="82f73-220">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-220">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="82f73-221">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-221">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="82f73-222">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="82f73-222">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="82f73-223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-223">Az.Sql</span></span>
* <span data-ttu-id="82f73-224">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="82f73-224">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="82f73-225">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="82f73-225">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82f73-226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82f73-226">Az.Websites</span></span>
* <span data-ttu-id="82f73-227">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="82f73-227">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="82f73-228">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="82f73-228">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82f73-229">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82f73-229">Az.Accounts</span></span>
* <span data-ttu-id="82f73-230">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="82f73-230">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82f73-231">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82f73-231">Az.AnalysisServices</span></span>
<span data-ttu-id="82f73-232">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="82f73-232">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-233">Az.Compute</span></span>
* <span data-ttu-id="82f73-234">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="82f73-234">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="82f73-235">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="82f73-235">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="82f73-236">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="82f73-236">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82f73-237">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82f73-237">Az.RecoveryServices</span></span>
<span data-ttu-id="82f73-238">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="82f73-238">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82f73-239">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-239">Az.Resources</span></span>
* <span data-ttu-id="82f73-240">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="82f73-240">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="82f73-241">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="82f73-241">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="82f73-242">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-242">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="82f73-243">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="82f73-243">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="82f73-244">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-244">Az.Sql</span></span>
* <span data-ttu-id="82f73-245">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="82f73-245">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="82f73-246">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-246">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="82f73-247">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="82f73-247">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="82f73-248">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="82f73-248">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82f73-249">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82f73-249">Az.Accounts</span></span>
* <span data-ttu-id="82f73-250">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="82f73-250">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="82f73-251">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="82f73-251">Az.AnalysisServices</span></span>
* <span data-ttu-id="82f73-252">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="82f73-252">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="82f73-253">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82f73-253">Az.RecoveryServices</span></span>
* <span data-ttu-id="82f73-254">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="82f73-254">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="82f73-255">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="82f73-255">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82f73-256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82f73-256">Az.Accounts</span></span>
* <span data-ttu-id="82f73-257">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="82f73-257">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="82f73-258">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-258">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82f73-259">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="82f73-259">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="82f73-260">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="82f73-260">Az.Aks</span></span>
* <span data-ttu-id="82f73-261">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-261">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="82f73-262">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82f73-262">Az.Automation</span></span>
* <span data-ttu-id="82f73-263">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="82f73-263">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="82f73-264">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-264">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="82f73-265">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="82f73-265">Az.Cdn</span></span>
* <span data-ttu-id="82f73-266">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-266">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-267">Az.Compute</span></span>
* <span data-ttu-id="82f73-268">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-268">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="82f73-269">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="82f73-269">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="82f73-270">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="82f73-270">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="82f73-271">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82f73-271">Az.ContainerRegistry</span></span>
* <span data-ttu-id="82f73-272">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-272">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="82f73-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="82f73-273">Az.DataFactory</span></span>
* <span data-ttu-id="82f73-274">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="82f73-274">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82f73-275">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82f73-275">Az.DataLakeStore</span></span>
* <span data-ttu-id="82f73-276">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-276">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="82f73-277">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="82f73-277">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="82f73-278">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-278">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82f73-279">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82f73-279">Az.IotHub</span></span>
* <span data-ttu-id="82f73-280">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82f73-280">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="82f73-281">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82f73-281">Az.KeyVault</span></span>
* <span data-ttu-id="82f73-282">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-282">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82f73-283">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-283">Az.Network</span></span>
* <span data-ttu-id="82f73-284">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-284">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="82f73-285">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-285">Az.Resources</span></span>
* <span data-ttu-id="82f73-286">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="82f73-286">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="82f73-287">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-287">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="82f73-288">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="82f73-288">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="82f73-289">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-289">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="82f73-290">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-290">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="82f73-291">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-291">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="82f73-292">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="82f73-292">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82f73-293">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82f73-293">Az.ServiceFabric</span></span>
* <span data-ttu-id="82f73-294">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="82f73-294">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="82f73-295">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="82f73-295">Fix some error messages.</span></span>
* <span data-ttu-id="82f73-296">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="82f73-296">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="82f73-297">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="82f73-297">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="82f73-298">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="82f73-298">Az.SignalR</span></span>
* <span data-ttu-id="82f73-299">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-299">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="82f73-300">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-300">Az.Sql</span></span>
* <span data-ttu-id="82f73-301">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-301">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82f73-302">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="82f73-302">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="82f73-303">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-303">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="82f73-304">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="82f73-304">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82f73-305">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82f73-305">Az.Storage</span></span>
* <span data-ttu-id="82f73-306">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-306">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82f73-307">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="82f73-307">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="82f73-308">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="82f73-308">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="82f73-309">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="82f73-309">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="82f73-310">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="82f73-310">Az.TrafficManager</span></span>
* <span data-ttu-id="82f73-311">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-311">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82f73-312">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82f73-312">Az.Websites</span></span>
* <span data-ttu-id="82f73-313">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="82f73-313">Update incorrect online help URLs</span></span>
* <span data-ttu-id="82f73-314">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="82f73-314">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="82f73-315">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="82f73-315">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="82f73-316">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="82f73-316">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="82f73-317">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82f73-317">Az.Accounts</span></span>
* <span data-ttu-id="82f73-318">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="82f73-318">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-319">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-319">Az.Compute</span></span>
* <span data-ttu-id="82f73-320">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="82f73-320">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="82f73-321">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="82f73-321">Updated the description of ID in help files</span></span>
* <span data-ttu-id="82f73-322">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="82f73-322">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82f73-323">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82f73-323">Az.DataLakeStore</span></span>
* <span data-ttu-id="82f73-324">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="82f73-324">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="82f73-325">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="82f73-325">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="82f73-326">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="82f73-326">Az.EventGrid</span></span>
* <span data-ttu-id="82f73-327">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="82f73-327">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="82f73-328">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="82f73-328">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="82f73-329">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="82f73-329">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="82f73-330">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="82f73-330">Event Time-To-Live,</span></span>
        - <span data-ttu-id="82f73-331">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="82f73-331">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="82f73-332">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="82f73-332">Dead letter endpoint.</span></span>
    - <span data-ttu-id="82f73-333">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="82f73-333">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="82f73-334">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="82f73-334">Event Time-To-Live,</span></span>
        - <span data-ttu-id="82f73-335">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="82f73-335">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="82f73-336">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="82f73-336">Dead letter endpoint.</span></span>
* <span data-ttu-id="82f73-337">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="82f73-337">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="82f73-338">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="82f73-338">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="82f73-339">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="82f73-339">Az.IotHub</span></span>
* <span data-ttu-id="82f73-340">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="82f73-340">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="82f73-341">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="82f73-341">Az.LogicApp</span></span>
* <span data-ttu-id="82f73-342">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="82f73-342">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="82f73-343">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-343">Az.Resources</span></span>
* <span data-ttu-id="82f73-344">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="82f73-344">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="82f73-345">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="82f73-345">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="82f73-346">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="82f73-346">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="82f73-347">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="82f73-347">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="82f73-348">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="82f73-348">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="82f73-349">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="82f73-349">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="82f73-350">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="82f73-350">Az.SignalR</span></span>
* <span data-ttu-id="82f73-351">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="82f73-351">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="82f73-352">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-352">Az.Sql</span></span>
* <span data-ttu-id="82f73-353">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="82f73-353">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="82f73-354">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82f73-354">Az.Storage</span></span>
* <span data-ttu-id="82f73-355">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="82f73-355">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="82f73-356">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="82f73-356">New-AzStorageContext</span></span>
* <span data-ttu-id="82f73-357">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="82f73-357">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="82f73-358">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="82f73-358">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82f73-359">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82f73-359">Az.Websites</span></span>
* <span data-ttu-id="82f73-360">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="82f73-360">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="82f73-361">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="82f73-361">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="82f73-362">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="82f73-362">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="82f73-363">一般</span><span class="sxs-lookup"><span data-stu-id="82f73-363">General</span></span>

- <span data-ttu-id="82f73-364">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="82f73-364">General Availability of Az Module</span></span>
- <span data-ttu-id="82f73-365">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="82f73-365">Online help for each module</span></span>
- <span data-ttu-id="82f73-366">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="82f73-366">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="82f73-367">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-367">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="82f73-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82f73-368">Az.Accounts</span></span>
- <span data-ttu-id="82f73-369">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="82f73-369">Changed from Az.Profile</span></span>
- <span data-ttu-id="82f73-370">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="82f73-370">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="82f73-371">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82f73-371">Az.ApiManagement</span></span>
- <span data-ttu-id="82f73-372">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="82f73-372">Fixes for #7002</span></span>
- <span data-ttu-id="82f73-373">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-373">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="82f73-374">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="82f73-374">Az.Batch</span></span>
- <span data-ttu-id="82f73-375">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="82f73-375">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="82f73-376">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="82f73-376">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="82f73-377">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-377">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="82f73-378">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="82f73-378">Az.Billing</span></span>
- <span data-ttu-id="82f73-379">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-379">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="82f73-380">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="82f73-380">Az.CognitivServices</span></span>
- <span data-ttu-id="82f73-381">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="82f73-381">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="82f73-382">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="82f73-382">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="82f73-383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="82f73-383">Az.ContainerInstance</span></span>
- <span data-ttu-id="82f73-384">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="82f73-384">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="82f73-385">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="82f73-385">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="82f73-386">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-386">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="82f73-387">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82f73-387">Az.DataLakeStore</span></span>
- <span data-ttu-id="82f73-388">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-388">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="82f73-389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="82f73-389">Az.Monitor</span></span>
- <span data-ttu-id="82f73-390">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-390">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="82f73-391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="82f73-391">Az.KeyVault</span></span>
- <span data-ttu-id="82f73-392">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="82f73-392">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="82f73-393">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="82f73-393">Az.MachineLearning</span></span>
- <span data-ttu-id="82f73-394">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-394">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="82f73-395">Az.Media</span><span class="sxs-lookup"><span data-stu-id="82f73-395">Az.Media</span></span>
- <span data-ttu-id="82f73-396">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="82f73-396">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="82f73-397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-397">Az.Network</span></span>
<span data-ttu-id="82f73-398">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="82f73-398">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="82f73-399">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="82f73-399">New cmdlets added:</span></span>
        - <span data-ttu-id="82f73-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82f73-400">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82f73-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82f73-401">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82f73-402">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82f73-402">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82f73-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82f73-403">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82f73-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82f73-404">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="82f73-405">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="82f73-405">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="82f73-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="82f73-406">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="82f73-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="82f73-407">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="82f73-408">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="82f73-408">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="82f73-409">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82f73-409">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="82f73-410">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="82f73-410">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="82f73-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="82f73-411">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="82f73-412">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="82f73-412">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="82f73-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="82f73-413">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="82f73-414">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="82f73-414">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="82f73-415">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-415">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="82f73-416">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82f73-416">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="82f73-417">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82f73-417">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="82f73-418">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="82f73-418">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="82f73-419">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-419">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="82f73-420">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-420">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="82f73-421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="82f73-421">Az.OperationalInsights</span></span>
- <span data-ttu-id="82f73-422">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-422">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="82f73-423">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82f73-423">Az.Profile</span></span>
- <span data-ttu-id="82f73-424">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="82f73-424">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="82f73-425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82f73-425">Az.RecoveryServices</span></span>
- <span data-ttu-id="82f73-426">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-426">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="82f73-427">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-427">Az.Resources</span></span>
- <span data-ttu-id="82f73-428">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-428">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="82f73-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82f73-429">Az.ServiceFabric</span></span>
- <span data-ttu-id="82f73-430">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="82f73-430">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="82f73-431">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-431">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="82f73-432">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="82f73-432">Az.SIgnalR</span></span>
- <span data-ttu-id="82f73-433">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="82f73-433">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="82f73-434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-434">Az.Sql</span></span>
- <span data-ttu-id="82f73-435">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="82f73-435">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="82f73-436">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="82f73-436">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="82f73-437">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-437">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="82f73-438">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82f73-438">Az.Storage</span></span>
- <span data-ttu-id="82f73-439">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-439">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="82f73-440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82f73-440">Az.Websites</span></span>
- <span data-ttu-id="82f73-441">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="82f73-441">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="82f73-442">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="82f73-442">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="82f73-443">一般</span><span class="sxs-lookup"><span data-stu-id="82f73-443">General</span></span>

* <span data-ttu-id="82f73-444">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="82f73-444">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="82f73-445">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-445">Az.Compute</span></span>

* <span data-ttu-id="82f73-446">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="82f73-446">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="82f73-447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82f73-447">Az.DataLakeStore</span></span>

* <span data-ttu-id="82f73-448">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="82f73-448">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="82f73-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="82f73-449">Az.FrontDoor</span></span>

* <span data-ttu-id="82f73-450">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="82f73-450">Fixed some broken links</span></span>
    - <span data-ttu-id="82f73-451">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="82f73-451">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="82f73-452">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="82f73-452">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="82f73-453">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="82f73-453">Az.RecoveryServices</span></span>

* <span data-ttu-id="82f73-454">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="82f73-454">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="82f73-455">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="82f73-455">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="82f73-456">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-456">Az.Resources</span></span>

* <span data-ttu-id="82f73-457">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="82f73-457">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="82f73-458">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="82f73-458">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="82f73-459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-459">Az.Sql</span></span>

* <span data-ttu-id="82f73-460">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="82f73-460">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="82f73-461">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-461">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="82f73-462">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="82f73-462">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="82f73-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="82f73-463">Az.Storage</span></span>

* <span data-ttu-id="82f73-464">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="82f73-464">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="82f73-465">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="82f73-465">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="82f73-466">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="82f73-466">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="82f73-467">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="82f73-467">Support Static Website configuration</span></span>
    - <span data-ttu-id="82f73-468">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="82f73-468">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="82f73-469">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="82f73-469">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="82f73-470">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82f73-470">Az.Websites</span></span>

* <span data-ttu-id="82f73-471">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="82f73-471">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="82f73-472">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="82f73-472">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="82f73-473">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="82f73-473">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="82f73-474">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="82f73-474">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="82f73-475">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="82f73-475">Az.ApiManagement</span></span>
* <span data-ttu-id="82f73-476">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="82f73-476">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="82f73-477">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="82f73-477">Az.Automation</span></span>
* <span data-ttu-id="82f73-478">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-478">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="82f73-479">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-479">Added Update Management cmdlets</span></span>
* <span data-ttu-id="82f73-480">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-480">Added Source Control cmdlets</span></span>
* <span data-ttu-id="82f73-481">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-481">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="82f73-482">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="82f73-482">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="82f73-483">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-483">Az.Compute</span></span>
* <span data-ttu-id="82f73-484">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="82f73-484">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="82f73-485">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="82f73-485">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="82f73-486">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="82f73-486">Az.ContainerInstance</span></span>
* <span data-ttu-id="82f73-487">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="82f73-487">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="82f73-488">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="82f73-488">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="82f73-489">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="82f73-489">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="82f73-490">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-490">Az.Network</span></span>
* <span data-ttu-id="82f73-491">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="82f73-491">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="82f73-492">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="82f73-492">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="82f73-493">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="82f73-493">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="82f73-494">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="82f73-494">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="82f73-495">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="82f73-495">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="82f73-496">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="82f73-496">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="82f73-497">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="82f73-497">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="82f73-498">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="82f73-498">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="82f73-499">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="82f73-499">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="82f73-500">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="82f73-500">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="82f73-501">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="82f73-501">Az.Relay</span></span>
* <span data-ttu-id="82f73-502">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="82f73-502">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="82f73-503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-503">Az.Resources</span></span>
* <span data-ttu-id="82f73-504">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="82f73-504">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="82f73-505">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="82f73-505">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="82f73-506">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="82f73-506">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="82f73-507">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82f73-507">Az.ServiceFabric</span></span>
* <span data-ttu-id="82f73-508">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="82f73-508">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="82f73-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-509">Az.Sql</span></span>
* <span data-ttu-id="82f73-510">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-510">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="82f73-511">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="82f73-511">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82f73-512">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="82f73-512">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82f73-513">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="82f73-513">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82f73-514">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="82f73-514">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="82f73-515">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82f73-515">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82f73-516">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82f73-516">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82f73-517">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82f73-517">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="82f73-518">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="82f73-518">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="82f73-519">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="82f73-519">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="82f73-520">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="82f73-520">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="82f73-521">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="82f73-521">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="82f73-522">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="82f73-522">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="82f73-523">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="82f73-523">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="82f73-524">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="82f73-524">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="82f73-525">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="82f73-525">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="82f73-526">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-526">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="82f73-527">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="82f73-527">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="82f73-528">一般</span><span class="sxs-lookup"><span data-stu-id="82f73-528">General</span></span>
* <span data-ttu-id="82f73-529">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="82f73-529">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="82f73-530">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82f73-530">Az.Profile</span></span>
* <span data-ttu-id="82f73-531">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="82f73-531">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="82f73-532">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="82f73-532">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="82f73-533">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="82f73-533">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="82f73-534">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="82f73-534">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="82f73-535">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-535">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="82f73-536">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-536">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="82f73-537">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-537">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="82f73-538">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82f73-538">Az.CognitiveServices</span></span>
* <span data-ttu-id="82f73-539">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="82f73-539">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-540">Az.Compute</span></span>
* <span data-ttu-id="82f73-541">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-541">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="82f73-542">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="82f73-542">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="82f73-543">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="82f73-543">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82f73-544">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82f73-544">Az.DataLakeStore</span></span>
* <span data-ttu-id="82f73-545">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="82f73-545">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="82f73-546">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="82f73-546">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="82f73-547">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="82f73-547">Az.Insights</span></span>
* <span data-ttu-id="82f73-548">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="82f73-548">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="82f73-549">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="82f73-549">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="82f73-550">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="82f73-550">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="82f73-551">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="82f73-551">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82f73-552">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-552">Az.Network</span></span>
* <span data-ttu-id="82f73-553">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="82f73-553">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="82f73-554">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="82f73-554">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="82f73-555">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="82f73-555">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="82f73-556">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="82f73-556">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="82f73-557">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="82f73-557">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="82f73-558">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="82f73-558">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="82f73-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="82f73-559">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="82f73-560">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="82f73-560">Az.PolicyInsights</span></span>
* <span data-ttu-id="82f73-561">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-561">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="82f73-562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-562">Az.Resources</span></span>
* <span data-ttu-id="82f73-563">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="82f73-563">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="82f73-564">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="82f73-564">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="82f73-565">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82f73-565">Az.ServiceBus</span></span>
* <span data-ttu-id="82f73-566">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="82f73-566">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="82f73-567">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="82f73-567">Az.ServiceFabric</span></span>
* <span data-ttu-id="82f73-568">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="82f73-568">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="82f73-569">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="82f73-569">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="82f73-570">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="82f73-570">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="82f73-571">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="82f73-571">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="82f73-572">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="82f73-572">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="82f73-573">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="82f73-573">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="82f73-574">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="82f73-574">Az.Profile</span></span>
* <span data-ttu-id="82f73-575">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-575">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="82f73-576">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="82f73-576">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-577">Az.Compute</span></span>
* <span data-ttu-id="82f73-578">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="82f73-578">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="82f73-579">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82f73-579">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="82f73-580">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="82f73-580">Az.DataLakeStore</span></span>
* <span data-ttu-id="82f73-581">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="82f73-581">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="82f73-582">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="82f73-582">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="82f73-583">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="82f73-583">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="82f73-584">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="82f73-584">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="82f73-585">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="82f73-585">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82f73-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-586">Az.Network</span></span>
* <span data-ttu-id="82f73-587">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="82f73-587">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="82f73-588">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82f73-588">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="82f73-589">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-589">Az.Resources</span></span>
* <span data-ttu-id="82f73-590">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="82f73-590">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="82f73-591">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="82f73-591">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="82f73-592">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="82f73-592">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="82f73-593">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="82f73-593">Azure.Storage</span></span>
* <span data-ttu-id="82f73-594">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-594">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="82f73-595">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="82f73-595">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="82f73-596">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="82f73-596">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="82f73-597">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="82f73-597">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="82f73-598">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="82f73-598">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="82f73-599">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="82f73-599">Az.CognitiveServices</span></span>
* <span data-ttu-id="82f73-600">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="82f73-600">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="82f73-601">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="82f73-601">Az.Compute</span></span>
* <span data-ttu-id="82f73-602">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="82f73-602">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="82f73-603">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="82f73-603">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="82f73-604">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="82f73-604">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="82f73-605">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="82f73-605">Az.DataFactoryV2</span></span>
* <span data-ttu-id="82f73-606">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="82f73-606">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="82f73-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="82f73-607">Az.Network</span></span>
* <span data-ttu-id="82f73-608">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="82f73-608">Added NetworkProfile functionality.</span></span> <span data-ttu-id="82f73-609">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-609">new cmdlets added</span></span>
    - <span data-ttu-id="82f73-610">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82f73-610">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="82f73-611">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82f73-611">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="82f73-612">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82f73-612">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="82f73-613">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="82f73-613">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="82f73-614">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="82f73-614">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="82f73-615">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="82f73-615">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="82f73-616">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="82f73-616">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="82f73-617">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-617">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="82f73-618">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="82f73-618">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="82f73-619">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="82f73-619">Az.RedisCache</span></span>
* <span data-ttu-id="82f73-620">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="82f73-620">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="82f73-621">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="82f73-621">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="82f73-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="82f73-622">Az.Resources</span></span>
* <span data-ttu-id="82f73-623">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="82f73-623">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="82f73-624">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="82f73-624">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="82f73-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="82f73-625">Az.Sql</span></span>
* <span data-ttu-id="82f73-626">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="82f73-626">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="82f73-627">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="82f73-627">Az.Websites</span></span>
* <span data-ttu-id="82f73-628">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="82f73-628">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="82f73-629">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="82f73-629">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="82f73-630">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="82f73-630">0.2.0 - September 2018</span></span>
 <span data-ttu-id="82f73-631">初始版本</span><span class="sxs-lookup"><span data-stu-id="82f73-631">Initial Release</span></span>