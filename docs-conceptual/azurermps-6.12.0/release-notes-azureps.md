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
ms.openlocfilehash: c60bc9197266cc1da37cc9af7baf03e7ba8fb7ac
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212621"
---
# <a name="release-notes"></a><span data-ttu-id="3d97a-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="3d97a-103">Release notes</span></span>

<span data-ttu-id="3d97a-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="3d97a-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="3d97a-105">6.12.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-106">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-107">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3d97a-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3d97a-108">將 Cmdlet Connect-AzureRmAccount 中的 param TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="3d97a-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3d97a-109">更新 Connect-AzureRmAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="3d97a-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="3d97a-110">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="3d97a-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3d97a-111">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3d97a-112">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3d97a-113">修正若未連線，'Disconnect-AzureRmAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="3d97a-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3d97a-114">AzureRM.Automation</span></span>
* <span data-ttu-id="3d97a-115">已將 Cmdlet DLL 檔案名稱重新命名為 Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="3d97a-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="3d97a-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d97a-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="3d97a-117">新增 Get-AzureRmCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="3d97a-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-118">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-119">新增 Add-AzureRmVmssVMDataDisk 和 Remove-AzureRmVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3d97a-120">Get-AzureRmVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="3d97a-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3d97a-121">已修正 SetAzureRmVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d97a-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d97a-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d97a-123">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="3d97a-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3d97a-124">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="3d97a-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3d97a-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="3d97a-125">AzureRM.Insights</span></span>
* <span data-ttu-id="3d97a-126">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="3d97a-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3d97a-127">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3d97a-128">已修正問題 #7513 [Insights] Set-AzureRMDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="3d97a-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3d97a-129">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="3d97a-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-130">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-131">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="3d97a-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3d97a-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3d97a-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3d97a-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3d97a-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3d97a-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3d97a-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3d97a-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3d97a-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3d97a-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3d97a-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3d97a-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3d97a-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3d97a-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d97a-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3d97a-139">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3d97a-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3d97a-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3d97a-141">已新增在復原服務中共用 Azure 檔案的支援。</span><span class="sxs-lookup"><span data-stu-id="3d97a-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-142">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-143">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="3d97a-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3d97a-144">允許使用 'Get-AzureRmResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="3d97a-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d97a-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d97a-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d97a-146">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="3d97a-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3d97a-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d97a-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3d97a-148">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="3d97a-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3d97a-149">修正 'Add-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="3d97a-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3d97a-150">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="3d97a-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3d97a-151">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="3d97a-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3d97a-152">修正 'Update-AzureRmServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="3d97a-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="3d97a-153">6.11.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-154">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-155">修正 CloudShell 中 Get-AzureRmSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="3d97a-156">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3d97a-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="3d97a-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="3d97a-157">AzureRM.Backup</span></span>
* <span data-ttu-id="3d97a-158">淘汰的 Azure 備份 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-159">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-160">已將新的大小新增至虛擬機器大小白名單，當使用 'New-AzureRmVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="3d97a-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="3d97a-161">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d97a-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d97a-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d97a-163">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3d97a-164">Get-AzureRmDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d97a-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3d97a-165">Add-AzureRmDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="3d97a-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3d97a-166">Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帳戶中修改指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d97a-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3d97a-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="3d97a-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-168">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-169">更新 Cmdlet Test-AzureRmNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="3d97a-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3d97a-170">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-171">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-172">修正當 Get-AzureRMRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3d97a-173">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="3d97a-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="3d97a-174">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3d97a-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-175">Azure.Storage</span></span>
* <span data-ttu-id="3d97a-176">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3d97a-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3d97a-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3d97a-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3d97a-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="3d97a-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d97a-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="3d97a-180">在沒有現有帳戶的情況下支援 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="3d97a-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-181">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-182">修正 Get-AzureRmVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="3d97a-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3d97a-183">已將 'SimpleParameterSet' 的範例新增到 New-AzureRmVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="3d97a-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="3d97a-184">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="3d97a-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3d97a-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d97a-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3d97a-186">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="3d97a-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-187">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-188">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="3d97a-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3d97a-189">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-189">new cmdlets added</span></span>
    - <span data-ttu-id="3d97a-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3d97a-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="3d97a-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3d97a-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="3d97a-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3d97a-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="3d97a-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3d97a-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="3d97a-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="3d97a-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3d97a-196">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="3d97a-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3d97a-197">已新增 New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap 和 Remove-AzureRmVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="3d97a-198">已新增 Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig 和 Remove-AzureRmNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="3d97a-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3d97a-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="3d97a-200">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="3d97a-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3d97a-201">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="3d97a-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-202">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-203">將遺漏的 -Mode 參數新增至 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3d97a-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="3d97a-204">修正 Get-AzureRmProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="3d97a-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d97a-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d97a-205">AzureRM.Sql</span></span>
* <span data-ttu-id="3d97a-206">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3d97a-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-207">AzureRM.Storage</span></span>
* <span data-ttu-id="3d97a-208">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="3d97a-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3d97a-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3d97a-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d97a-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d97a-210">AzureRM.Websites</span></span>
* <span data-ttu-id="3d97a-211">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="3d97a-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3d97a-212">新 Cmdlet New-AzureRMWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="3d97a-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="3d97a-213">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d97a-214">一般</span><span class="sxs-lookup"><span data-stu-id="3d97a-214">General</span></span>
* <span data-ttu-id="3d97a-215">已將 AzureRM.SignalR 新增至 AzureRM 彙總模組</span><span class="sxs-lookup"><span data-stu-id="3d97a-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-216">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-217">儲存體通用程式碼的小幅變更</span><span class="sxs-lookup"><span data-stu-id="3d97a-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="3d97a-218">已更新說明檔以包含完整的參數類型。</span><span class="sxs-lookup"><span data-stu-id="3d97a-218">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="3d97a-219">已變更 - 非強制性的 ServicePrincipal 位在 ServicePrincipalCertificateWithSubscriptionId 參數集</span><span class="sxs-lookup"><span data-stu-id="3d97a-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="3d97a-220">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-220">Azure.Storage</span></span>
* <span data-ttu-id="3d97a-221">支援使用 OAuth 建立儲存體內容。</span><span class="sxs-lookup"><span data-stu-id="3d97a-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="3d97a-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d97a-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="3d97a-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="3d97a-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="3d97a-224">已在 CDN 定價 SKU 中新增 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3d97a-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-225">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-226">將金鑰保存庫和儲存體上的相依性移至一般相依性</span><span class="sxs-lookup"><span data-stu-id="3d97a-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="3d97a-227">對 AEM Cmdlet 新增更多的虛擬機器大小支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="3d97a-228">將 PublicIPPrefix 參數新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="3d97a-229">將 ResourceId 參數新增至 Invoke-AzureRmVMRunCommand Cmdelt</span><span class="sxs-lookup"><span data-stu-id="3d97a-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="3d97a-230">新增 Invoke-AzureRmVmssVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="3d97a-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="3d97a-231">AzureRM.Dns</span></span>
* <span data-ttu-id="3d97a-232">已新增建立 DNS 記錄時的別名記錄支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3d97a-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="3d97a-233">AzureRM.Insights</span></span>
* <span data-ttu-id="3d97a-234">已修正問題 #6833 和 #7102 (診斷設定區域)</span><span class="sxs-lookup"><span data-stu-id="3d97a-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="3d97a-235">建立和列出/取得診斷設定時的預設名稱問題 (例如 'service')</span><span class="sxs-lookup"><span data-stu-id="3d97a-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="3d97a-236">以類別建立診斷設定的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="3d97a-237">已新增計量時間粒紋參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="3d97a-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="3d97a-238">Timegrains 參數還是可用 (這是非中斷性變更)，但會在後端中遭到忽略，因為只有 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="3d97a-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-239">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-240">LoadBalancer Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="3d97a-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="3d97a-241">LoadBalancerInboundNatPoolConfig：已新增 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="3d97a-242">LoadBalancerInboundNatRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="3d97a-243">LoadBalancerRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="3d97a-244">LoadBalancerProbeConfig：已為 Protocol 參數新增 "Https" 值的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="3d97a-245">已為新 LoadBalancer 的子資源 OutboundRule 新增命令</span><span class="sxs-lookup"><span data-stu-id="3d97a-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="3d97a-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="3d97a-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="3d97a-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="3d97a-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="3d97a-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="3d97a-251">已為 PSNetworkInterface 新增 HostedWorkloads 屬性</span><span class="sxs-lookup"><span data-stu-id="3d97a-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="3d97a-252">已為以下功能新增 Cmdlet：由 ARM 支援的 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="3d97a-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="3d97a-253">已新增 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3d97a-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="3d97a-254">已新增 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3d97a-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="3d97a-255">已新增 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3d97a-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="3d97a-256">已新增 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="3d97a-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="3d97a-257">已新增 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3d97a-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="3d97a-258">已新增 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="3d97a-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="3d97a-259">已新增 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3d97a-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="3d97a-260">已新增 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="3d97a-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="3d97a-261">已新增 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3d97a-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="3d97a-262">已新增 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3d97a-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="3d97a-263">已在應用程式閘道中新增受信任根憑證和自動調整組態的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="3d97a-264">已新增的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="3d97a-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="3d97a-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3d97a-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3d97a-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3d97a-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3d97a-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="3d97a-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="3d97a-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="3d97a-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="3d97a-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="3d97a-274">已使用選擇性參數 TrustedRootCertificate 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="3d97a-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d97a-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="3d97a-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d97a-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="3d97a-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3d97a-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="3d97a-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="3d97a-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="3d97a-279">已使用選擇性參數 AutoscaleConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="3d97a-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d97a-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="3d97a-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d97a-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="3d97a-282">為介面端點 Get-AzureInterfaceEndpoint 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="3d97a-283">已在子網路中新增多個位址前置詞的支援。</span><span class="sxs-lookup"><span data-stu-id="3d97a-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="3d97a-284">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="3d97a-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="3d97a-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="3d97a-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="3d97a-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="3d97a-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="3d97a-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="3d97a-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="3d97a-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="3d97a-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="3d97a-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="3d97a-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="3d97a-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="3d97a-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="3d97a-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="3d97a-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="3d97a-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="3d97a-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="3d97a-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="3d97a-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="3d97a-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3d97a-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="3d97a-304">為子網路委派新增 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="3d97a-305">New-AzureRmDelegation：建立可新增至子網路的新委派</span><span class="sxs-lookup"><span data-stu-id="3d97a-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="3d97a-306">Remove-AzureRmDelegation：用於子網路，可從該子網路中移除提供的委派名稱</span><span class="sxs-lookup"><span data-stu-id="3d97a-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="3d97a-307">Add-AzureRmDelegation：用於子網路，可將提供的服務名稱新增為該子網路的委派</span><span class="sxs-lookup"><span data-stu-id="3d97a-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="3d97a-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="3d97a-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="3d97a-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="3d97a-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="3d97a-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3d97a-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3d97a-311">支援受控磁碟</span><span class="sxs-lookup"><span data-stu-id="3d97a-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="3d97a-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3d97a-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="3d97a-313">已更新深入解析相依性。</span><span class="sxs-lookup"><span data-stu-id="3d97a-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-314">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-315">使用新參數 RollbackAction 更新 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3d97a-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="3d97a-316">使用新參數新增 OnErrorDeployment 的支援。</span><span class="sxs-lookup"><span data-stu-id="3d97a-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="3d97a-317">支援原則指派上的受控識別。</span><span class="sxs-lookup"><span data-stu-id="3d97a-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="3d97a-318">以 'New-AzureRmPolicyAssignment' 指派原則時不再需要具有預設值的參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="3d97a-319">新增 Get-AzureRmPolicyAlias Cmdlet 來擷取原則別名</span><span class="sxs-lookup"><span data-stu-id="3d97a-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d97a-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d97a-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d97a-321">已修正問題 #7161</span><span class="sxs-lookup"><span data-stu-id="3d97a-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="3d97a-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="3d97a-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="3d97a-323">將 SKU 名稱更新為 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="3d97a-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="3d97a-324">將版本欄位新增至 PSSignalRResource 物件，以及將連接字串新增至 PSSignalRKeys 物件。</span><span class="sxs-lookup"><span data-stu-id="3d97a-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3d97a-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-325">AzureRM.Storage</span></span>
* <span data-ttu-id="3d97a-326">在 AzureRm.Storage 中支援不變原則</span><span class="sxs-lookup"><span data-stu-id="3d97a-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="3d97a-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3d97a-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="3d97a-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3d97a-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="3d97a-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3d97a-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="3d97a-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3d97a-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="3d97a-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3d97a-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="3d97a-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="3d97a-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="3d97a-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="3d97a-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="3d97a-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3d97a-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="3d97a-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3d97a-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="3d97a-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3d97a-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="3d97a-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3d97a-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d97a-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d97a-338">AzureRM.Websites</span></span>
* <span data-ttu-id="3d97a-339">已新增兩個 Cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3d97a-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="3d97a-340">New-AzureRmAppServicePlan - 已新增 HyperV 切換以使用 Windows 容器建立 App Service 方案</span><span class="sxs-lookup"><span data-stu-id="3d97a-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="3d97a-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 已新增參數 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) 來建立和管理 Windows 容器應用程式</span><span class="sxs-lookup"><span data-stu-id="3d97a-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="3d97a-342">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d97a-343">一般</span><span class="sxs-lookup"><span data-stu-id="3d97a-343">General</span></span>
* <span data-ttu-id="3d97a-344">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3d97a-345">已更新通用執行階段組件</span><span class="sxs-lookup"><span data-stu-id="3d97a-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d97a-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d97a-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d97a-347">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3d97a-348">已修正的問題 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="3d97a-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="3d97a-349">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlets 目前處理相對路徑</span><span class="sxs-lookup"><span data-stu-id="3d97a-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="3d97a-350">已修正的問題 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="3d97a-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="3d97a-351">CertificateInformation 為可設定的屬性，允許 Set-AzureRmApiManagement Cmdlet 正常運作。</span><span class="sxs-lookup"><span data-stu-id="3d97a-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="3d97a-352">已藉由升級至 4.0.4-preview NuGet 而修正</span><span class="sxs-lookup"><span data-stu-id="3d97a-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="3d97a-353">已修正的問題 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="3d97a-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="3d97a-354">已修正依產品名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="3d97a-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="3d97a-355">已修正的問題 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="3d97a-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="3d97a-356">已修正依 API 名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="3d97a-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="3d97a-357">已新增對 AzureMonitor 記錄器的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-358">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-359">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="3d97a-360">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="3d97a-361">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="3d97a-362">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="3d97a-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-363">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-364">已將預設的 Cmdlet 輸出表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="3d97a-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3d97a-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3d97a-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3d97a-366">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="3d97a-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="3d97a-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-367">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-368">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d97a-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d97a-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d97a-370">已修正的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d97a-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d97a-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d97a-372">已新增對 MultiValue 路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="3d97a-373">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="3d97a-374">已新增對子網路路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="3d97a-375">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="3d97a-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="3d97a-376">已新增對設定檔中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="3d97a-377">已新增對設定檔中預期狀態碼的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="3d97a-378">已新增對端點中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="3d97a-379">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d97a-380">一般</span><span class="sxs-lookup"><span data-stu-id="3d97a-380">General</span></span>
* <span data-ttu-id="3d97a-381">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-382">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-383">已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖</span><span class="sxs-lookup"><span data-stu-id="3d97a-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-384">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-385">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="3d97a-386">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="3d97a-387">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="3d97a-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="3d97a-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="3d97a-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="3d97a-389">修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-390">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-391">已將預設模式表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="3d97a-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3d97a-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3d97a-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3d97a-393">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="3d97a-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-394">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-395">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d97a-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d97a-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d97a-397">修正問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d97a-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d97a-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d97a-399">支援 MultiValue 路由方法</span><span class="sxs-lookup"><span data-stu-id="3d97a-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="3d97a-400">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="3d97a-401">支援子網路路由方法</span><span class="sxs-lookup"><span data-stu-id="3d97a-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="3d97a-402">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="3d97a-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="3d97a-403">支援設定檔中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="3d97a-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="3d97a-404">支援設定檔中的預期狀態碼</span><span class="sxs-lookup"><span data-stu-id="3d97a-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="3d97a-405">支援端點中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="3d97a-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d97a-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d97a-406">AzureRM.Websites</span></span>
* <span data-ttu-id="3d97a-407">已修正未正確設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="3d97a-408">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-409">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-410">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3d97a-411">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="3d97a-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="3d97a-412">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="3d97a-413">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="3d97a-414">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-414">Azure.Storage</span></span>
* <span data-ttu-id="3d97a-415">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="3d97a-415">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="3d97a-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="3d97a-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3d97a-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d97a-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3d97a-418">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="3d97a-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d97a-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="3d97a-420">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d97a-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d97a-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d97a-422">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="3d97a-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3d97a-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="3d97a-424">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="3d97a-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3d97a-425">AzureRM.Automation</span></span>
* <span data-ttu-id="3d97a-426">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="3d97a-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="3d97a-427">AzureRM.Backup</span></span>
* <span data-ttu-id="3d97a-428">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="3d97a-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="3d97a-429">AzureRM.Batch</span></span>
* <span data-ttu-id="3d97a-430">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="3d97a-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="3d97a-431">AzureRM.Billing</span></span>
* <span data-ttu-id="3d97a-432">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="3d97a-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="3d97a-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="3d97a-434">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="3d97a-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3d97a-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="3d97a-436">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-437">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-438">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3d97a-439">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="3d97a-440">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="3d97a-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="3d97a-441">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="3d97a-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="3d97a-442">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="3d97a-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="3d97a-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="3d97a-444">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="3d97a-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3d97a-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="3d97a-446">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="3d97a-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3d97a-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="3d97a-448">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="3d97a-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="3d97a-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="3d97a-450">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3d97a-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d97a-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3d97a-452">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="3d97a-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3d97a-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="3d97a-454">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d97a-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d97a-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d97a-456">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="3d97a-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="3d97a-457">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="3d97a-458">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3d97a-459">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="3d97a-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="3d97a-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="3d97a-461">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="3d97a-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="3d97a-462">AzureRM.Dns</span></span>
* <span data-ttu-id="3d97a-463">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="3d97a-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3d97a-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="3d97a-465">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3d97a-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d97a-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="3d97a-467">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="3d97a-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3d97a-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="3d97a-469">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3d97a-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="3d97a-470">AzureRM.Insights</span></span>
* <span data-ttu-id="3d97a-471">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="3d97a-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="3d97a-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="3d97a-473">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d97a-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d97a-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d97a-475">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="3d97a-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3d97a-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="3d97a-477">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="3d97a-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3d97a-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="3d97a-479">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="3d97a-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="3d97a-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="3d97a-481">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="3d97a-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3d97a-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="3d97a-483">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="3d97a-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="3d97a-484">AzureRM.Media</span></span>
* <span data-ttu-id="3d97a-485">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-486">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-487">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="3d97a-488">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="3d97a-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3d97a-489">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="3d97a-490">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="3d97a-491">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="3d97a-492">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3d97a-493">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="3d97a-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="3d97a-494">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="3d97a-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="3d97a-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3d97a-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="3d97a-496">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="3d97a-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d97a-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="3d97a-498">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3d97a-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d97a-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3d97a-500">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="3d97a-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3d97a-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="3d97a-502">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="3d97a-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3d97a-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="3d97a-504">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3d97a-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3d97a-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3d97a-506">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="3d97a-507">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="3d97a-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="3d97a-508">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="3d97a-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="3d97a-509">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="3d97a-510">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="3d97a-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="3d97a-511">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3d97a-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="3d97a-512">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="3d97a-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="3d97a-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3d97a-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3d97a-514">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="3d97a-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3d97a-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="3d97a-516">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="3d97a-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="3d97a-517">AzureRM.Relay</span></span>
* <span data-ttu-id="3d97a-518">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-519">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-520">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="3d97a-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="3d97a-521">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="3d97a-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="3d97a-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d97a-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d97a-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d97a-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d97a-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d97a-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d97a-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d97a-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d97a-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3d97a-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="3d97a-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="3d97a-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="3d97a-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="3d97a-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="3d97a-529">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="3d97a-530">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="3d97a-531">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="3d97a-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="3d97a-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="3d97a-533">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d97a-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d97a-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d97a-535">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3d97a-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d97a-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3d97a-537">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d97a-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d97a-538">AzureRM.Sql</span></span>
* <span data-ttu-id="3d97a-539">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3d97a-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-540">AzureRM.Storage</span></span>
* <span data-ttu-id="3d97a-541">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="3d97a-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="3d97a-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="3d97a-543">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="3d97a-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="3d97a-544">AzureRM.Tags</span></span>
* <span data-ttu-id="3d97a-545">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d97a-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d97a-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d97a-547">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="3d97a-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="3d97a-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="3d97a-549">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d97a-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d97a-550">AzureRM.Websites</span></span>
* <span data-ttu-id="3d97a-551">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="3d97a-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="3d97a-552">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d97a-553">一般</span><span class="sxs-lookup"><span data-stu-id="3d97a-553">General</span></span>
* <span data-ttu-id="3d97a-554">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="3d97a-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-555">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-556">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="3d97a-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="3d97a-557">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3d97a-558">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-558">Azure.Storage</span></span>
* <span data-ttu-id="3d97a-559">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="3d97a-560">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="3d97a-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d97a-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d97a-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d97a-562">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="3d97a-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="3d97a-563">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="3d97a-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="3d97a-564">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="3d97a-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="3d97a-565">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="3d97a-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="3d97a-566">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="3d97a-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="3d97a-567">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="3d97a-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-568">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-569">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="3d97a-570">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="3d97a-571">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="3d97a-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="3d97a-572">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="3d97a-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="3d97a-573">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="3d97a-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="3d97a-574">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="3d97a-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="3d97a-575">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="3d97a-576">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="3d97a-577">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="3d97a-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="3d97a-578">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="3d97a-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3d97a-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d97a-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3d97a-580">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="3d97a-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="3d97a-581">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="3d97a-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="3d97a-582">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="3d97a-583">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d97a-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d97a-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d97a-585">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="3d97a-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3d97a-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d97a-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="3d97a-587">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="3d97a-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="3d97a-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="3d97a-588">AzureRM.Insights</span></span>
* <span data-ttu-id="3d97a-589">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="3d97a-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="3d97a-590">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="3d97a-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d97a-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d97a-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d97a-592">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-593">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-594">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="3d97a-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-595">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-596">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="3d97a-597">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="3d97a-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d97a-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d97a-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d97a-599">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="3d97a-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="3d97a-600">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="3d97a-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d97a-601">AzureRM.Sql</span></span>
* <span data-ttu-id="3d97a-602">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="3d97a-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="3d97a-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3d97a-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="3d97a-604">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="3d97a-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="3d97a-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="3d97a-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="3d97a-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="3d97a-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="3d97a-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="3d97a-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="3d97a-608">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="3d97a-609">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="3d97a-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="3d97a-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-610">AzureRM.Storage</span></span>
* <span data-ttu-id="3d97a-611">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="3d97a-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="3d97a-612">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="3d97a-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="3d97a-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d97a-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="3d97a-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d97a-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="3d97a-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d97a-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="3d97a-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="3d97a-616">AzureRM.Tags</span></span>
* <span data-ttu-id="3d97a-617">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="3d97a-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="3d97a-618">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-619">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-620">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="3d97a-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3d97a-621">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-621">Azure.Storage</span></span>
* <span data-ttu-id="3d97a-622">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="3d97a-622">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="3d97a-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3d97a-623">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="3d97a-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3d97a-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3d97a-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d97a-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3d97a-626">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="3d97a-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="3d97a-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="3d97a-627">AzureRM.Automation</span></span>
* <span data-ttu-id="3d97a-628">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-629">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-630">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3d97a-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="3d97a-631">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="3d97a-632">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="3d97a-633">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="3d97a-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="3d97a-634">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="3d97a-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3d97a-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d97a-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="3d97a-636">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="3d97a-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d97a-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d97a-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d97a-638">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="3d97a-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="3d97a-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3d97a-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="3d97a-640">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="3d97a-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-641">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-642">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="3d97a-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="3d97a-643">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="3d97a-644">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="3d97a-645">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="3d97a-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="3d97a-646">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="3d97a-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="3d97a-647">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="3d97a-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="3d97a-648">AzureRM.Relay</span></span>
* <span data-ttu-id="3d97a-649">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-650">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-651">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="3d97a-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="3d97a-652">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3d97a-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="3d97a-653">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="3d97a-654">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="3d97a-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="3d97a-655">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="3d97a-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d97a-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d97a-657">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="3d97a-658">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="3d97a-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="3d97a-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d97a-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3d97a-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d97a-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3d97a-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d97a-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3d97a-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d97a-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="3d97a-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="3d97a-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="3d97a-664">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="3d97a-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3d97a-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d97a-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3d97a-666">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d97a-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d97a-667">AzureRM.Sql</span></span>
* <span data-ttu-id="3d97a-668">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="3d97a-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="3d97a-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="3d97a-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d97a-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d97a-671">AzureRM.Websites</span></span>
* <span data-ttu-id="3d97a-672">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="3d97a-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="3d97a-673">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="3d97a-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="3d97a-674">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="3d97a-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="3d97a-675">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3d97a-676">一般</span><span class="sxs-lookup"><span data-stu-id="3d97a-676">General</span></span>
* <span data-ttu-id="3d97a-677">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="3d97a-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-678">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-679">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="3d97a-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-680">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-681">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="3d97a-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="3d97a-682">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="3d97a-683">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="3d97a-684">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="3d97a-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="3d97a-685">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d97a-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="3d97a-686">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="3d97a-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="3d97a-687">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d97a-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="3d97a-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3d97a-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="3d97a-689">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="3d97a-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="3d97a-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3d97a-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="3d97a-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3d97a-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="3d97a-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3d97a-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d97a-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d97a-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d97a-694">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="3d97a-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="3d97a-695">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3d97a-696">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="3d97a-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="3d97a-697">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="3d97a-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="3d97a-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="3d97a-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="3d97a-699">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3d97a-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="3d97a-700">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="3d97a-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="3d97a-701">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="3d97a-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="3d97a-702">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="3d97a-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d97a-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d97a-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d97a-704">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-705">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-706">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="3d97a-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="3d97a-707">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="3d97a-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="3d97a-708">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3d97a-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="3d97a-709">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="3d97a-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="3d97a-710">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3d97a-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3d97a-711">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3d97a-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3d97a-712">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="3d97a-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="3d97a-713">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3d97a-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3d97a-714">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3d97a-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3d97a-715">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3d97a-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3d97a-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3d97a-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3d97a-717">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="3d97a-718">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="3d97a-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="3d97a-719">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3d97a-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-720">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-721">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="3d97a-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="3d97a-722">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="3d97a-723">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="3d97a-724">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="3d97a-725">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="3d97a-726">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="3d97a-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="3d97a-727">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="3d97a-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="3d97a-728">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="3d97a-729">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="3d97a-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="3d97a-730">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="3d97a-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="3d97a-731">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="3d97a-732">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="3d97a-733">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="3d97a-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3d97a-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="3d97a-735">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="3d97a-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d97a-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d97a-736">AzureRM.Sql</span></span>
* <span data-ttu-id="3d97a-737">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="3d97a-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="3d97a-738">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="3d97a-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="3d97a-739">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-740">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-741">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="3d97a-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="3d97a-742">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="3d97a-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="3d97a-743">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3d97a-743">Azure.Storage</span></span>
* <span data-ttu-id="3d97a-744">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="3d97a-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-745">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-746">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="3d97a-747">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="3d97a-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3d97a-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="3d97a-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3d97a-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="3d97a-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="3d97a-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="3d97a-751">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="3d97a-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="3d97a-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d97a-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="3d97a-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d97a-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="3d97a-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d97a-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="3d97a-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3d97a-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="3d97a-756">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="3d97a-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="3d97a-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d97a-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="3d97a-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="3d97a-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="3d97a-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="3d97a-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="3d97a-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d97a-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="3d97a-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d97a-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="3d97a-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d97a-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="3d97a-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3d97a-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="3d97a-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3d97a-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="3d97a-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="3d97a-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="3d97a-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="3d97a-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="3d97a-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="3d97a-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="3d97a-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3d97a-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="3d97a-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3d97a-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="3d97a-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="3d97a-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="3d97a-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3d97a-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="3d97a-772">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="3d97a-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="3d97a-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d97a-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d97a-774">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="3d97a-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="3d97a-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3d97a-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="3d97a-776">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="3d97a-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="3d97a-777">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="3d97a-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="3d97a-778">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="3d97a-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="3d97a-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3d97a-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3d97a-780">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="3d97a-781">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d97a-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d97a-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d97a-782">AzureRM.Sql</span></span>
* <span data-ttu-id="3d97a-783">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d97a-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d97a-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d97a-785">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d97a-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d97a-786">AzureRM.Websites</span></span>
* <span data-ttu-id="3d97a-787">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="3d97a-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="3d97a-788">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="3d97a-789">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="3d97a-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3d97a-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="3d97a-791">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="3d97a-792">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-793">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-794">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="3d97a-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="3d97a-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="3d97a-795">AzureRM.Compute</span></span>
* <span data-ttu-id="3d97a-796">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="3d97a-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="3d97a-797">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="3d97a-798">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="3d97a-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="3d97a-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3d97a-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="3d97a-800">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="3d97a-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="3d97a-801">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="3d97a-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="3d97a-802">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="3d97a-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="3d97a-803">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="3d97a-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="3d97a-804">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="3d97a-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="3d97a-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3d97a-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="3d97a-806">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="3d97a-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-807">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-808">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="3d97a-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="3d97a-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="3d97a-809">AzureRM.Resources</span></span>
* <span data-ttu-id="3d97a-810">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="3d97a-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="3d97a-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="3d97a-812">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="3d97a-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d97a-813">AzureRM.Sql</span></span>
* <span data-ttu-id="3d97a-814">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d97a-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="3d97a-815">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d97a-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3d97a-816">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d97a-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3d97a-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3d97a-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3d97a-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3d97a-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3d97a-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d97a-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="3d97a-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="3d97a-820">AzureRM.Websites</span></span>
* <span data-ttu-id="3d97a-821">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="3d97a-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="3d97a-822">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="3d97a-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="3d97a-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="3d97a-823">AzureRM.Profile</span></span>
* <span data-ttu-id="3d97a-824">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="3d97a-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="3d97a-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3d97a-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="3d97a-826">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="3d97a-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="3d97a-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3d97a-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="3d97a-828">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="3d97a-829">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="3d97a-830">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="3d97a-831">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="3d97a-832">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="3d97a-833">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="3d97a-834">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="3d97a-834">Added support for MSI identity</span></span>
* <span data-ttu-id="3d97a-835">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="3d97a-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="3d97a-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="3d97a-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="3d97a-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="3d97a-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="3d97a-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="3d97a-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="3d97a-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="3d97a-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="3d97a-840">AzureRM.Batch</span></span>
* <span data-ttu-id="3d97a-841">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="3d97a-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="3d97a-842">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="3d97a-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="3d97a-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="3d97a-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="3d97a-844">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="3d97a-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="3d97a-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3d97a-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="3d97a-846">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="3d97a-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="3d97a-847">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="3d97a-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="3d97a-848">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="3d97a-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="3d97a-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="3d97a-849">AzureRM.Network</span></span>
* <span data-ttu-id="3d97a-850">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="3d97a-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="3d97a-851">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="3d97a-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="3d97a-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d97a-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="3d97a-853">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="3d97a-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="3d97a-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3d97a-855">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="3d97a-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="3d97a-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="3d97a-857">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="3d97a-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="3d97a-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="3d97a-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="3d97a-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3d97a-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="3d97a-860">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="3d97a-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="3d97a-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="3d97a-861">AzureRM.Sql</span></span>
* <span data-ttu-id="3d97a-862">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="3d97a-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="3d97a-863">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="3d97a-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="3d97a-864">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="3d97a-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="3d97a-865">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="3d97a-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="3d97a-866">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="3d97a-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="3d97a-867">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d97a-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="3d97a-868">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="3d97a-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="3d97a-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3d97a-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="3d97a-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3d97a-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="3d97a-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d97a-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="3d97a-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3d97a-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="3d97a-873">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="3d97a-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
