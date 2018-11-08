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
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2018
ms.locfileid: "50971970"
---
# <a name="release-notes"></a><span data-ttu-id="c91ba-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="c91ba-103">Release notes</span></span>

<span data-ttu-id="c91ba-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="c91ba-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="c91ba-105">6.11.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-106">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-107">修正 CloudShell 中 Get-AzureRmSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="c91ba-108">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c91ba-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c91ba-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c91ba-109">AzureRM.Backup</span></span>
* <span data-ttu-id="c91ba-110">淘汰的 Azure 備份 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-111">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-112">已將新的大小新增至虛擬機器大小白名單，當使用 'New-AzureRmVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="c91ba-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="c91ba-113">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c91ba-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c91ba-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c91ba-115">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c91ba-116">Get-AzureRmDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c91ba-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c91ba-117">Add-AzureRmDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="c91ba-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c91ba-118">Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帳戶中修改指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c91ba-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c91ba-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="c91ba-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-120">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-121">更新 Cmdlet Test-AzureRmNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="c91ba-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c91ba-122">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-123">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-124">修正當 Get-AzureRMRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c91ba-125">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="c91ba-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="c91ba-126">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c91ba-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-127">Azure.Storage</span></span>
* <span data-ttu-id="c91ba-128">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c91ba-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c91ba-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c91ba-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c91ba-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c91ba-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c91ba-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c91ba-132">在沒有現有帳戶的情況下支援 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="c91ba-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-133">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-134">修正 Get-AzureRmVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="c91ba-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c91ba-135">已將 'SimpleParameterSet' 的範例新增到 New-AzureRmVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="c91ba-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="c91ba-136">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="c91ba-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c91ba-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c91ba-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c91ba-138">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="c91ba-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-139">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-140">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="c91ba-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c91ba-141">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-141">new cmdlets added</span></span>
    - <span data-ttu-id="c91ba-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c91ba-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c91ba-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c91ba-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c91ba-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c91ba-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c91ba-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c91ba-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c91ba-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="c91ba-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c91ba-148">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="c91ba-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c91ba-149">已新增 New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap 和 Remove-AzureRmVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="c91ba-150">已新增 Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig 和 Remove-AzureRmNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c91ba-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c91ba-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c91ba-152">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="c91ba-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c91ba-153">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="c91ba-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-154">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-155">將遺漏的 -Mode 參數新增至 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c91ba-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="c91ba-156">修正 Get-AzureRmProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="c91ba-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c91ba-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c91ba-157">AzureRM.Sql</span></span>
* <span data-ttu-id="c91ba-158">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c91ba-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-159">AzureRM.Storage</span></span>
* <span data-ttu-id="c91ba-160">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="c91ba-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c91ba-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c91ba-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c91ba-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c91ba-162">AzureRM.Websites</span></span>
* <span data-ttu-id="c91ba-163">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="c91ba-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c91ba-164">新 Cmdlet New-AzureRMWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="c91ba-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="c91ba-165">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c91ba-166">一般</span><span class="sxs-lookup"><span data-stu-id="c91ba-166">General</span></span>
* <span data-ttu-id="c91ba-167">已將 AzureRM.SignalR 新增至 AzureRM 彙總模組</span><span class="sxs-lookup"><span data-stu-id="c91ba-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-168">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-169">儲存體通用程式碼的小幅變更</span><span class="sxs-lookup"><span data-stu-id="c91ba-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="c91ba-170">已更新說明檔以包含完整的參數類型。</span><span class="sxs-lookup"><span data-stu-id="c91ba-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="c91ba-171">已變更 - 非強制性的 ServicePrincipal 位在 ServicePrincipalCertificateWithSubscriptionId 參數集</span><span class="sxs-lookup"><span data-stu-id="c91ba-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="c91ba-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-172">Azure.Storage</span></span>
* <span data-ttu-id="c91ba-173">支援使用 OAuth 建立儲存體內容。</span><span class="sxs-lookup"><span data-stu-id="c91ba-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="c91ba-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c91ba-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c91ba-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c91ba-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="c91ba-176">已在 CDN 定價 SKU 中新增 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c91ba-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-177">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-178">將金鑰保存庫和儲存體上的相依性移至一般相依性</span><span class="sxs-lookup"><span data-stu-id="c91ba-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="c91ba-179">對 AEM Cmdlet 新增更多的虛擬機器大小支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="c91ba-180">將 PublicIPPrefix 參數新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c91ba-181">將 ResourceId 參數新增至 Invoke-AzureRmVMRunCommand Cmdelt</span><span class="sxs-lookup"><span data-stu-id="c91ba-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="c91ba-182">新增 Invoke-AzureRmVmssVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c91ba-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c91ba-183">AzureRM.Dns</span></span>
* <span data-ttu-id="c91ba-184">已新增建立 DNS 記錄時的別名記錄支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c91ba-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c91ba-185">AzureRM.Insights</span></span>
* <span data-ttu-id="c91ba-186">已修正問題 #6833 和 #7102 (診斷設定區域)</span><span class="sxs-lookup"><span data-stu-id="c91ba-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="c91ba-187">建立和列出/取得診斷設定時的預設名稱問題 (例如 'service')</span><span class="sxs-lookup"><span data-stu-id="c91ba-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="c91ba-188">以類別建立診斷設定的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="c91ba-189">已新增計量時間粒紋參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="c91ba-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="c91ba-190">Timegrains 參數還是可用 (這是非中斷性變更)，但會在後端中遭到忽略，因為只有 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="c91ba-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-191">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-192">LoadBalancer Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="c91ba-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="c91ba-193">LoadBalancerInboundNatPoolConfig：已新增 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="c91ba-194">LoadBalancerInboundNatRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c91ba-195">LoadBalancerRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c91ba-196">LoadBalancerProbeConfig：已為 Protocol 參數新增 "Https" 值的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="c91ba-197">已為新 LoadBalancer 的子資源 OutboundRule 新增命令</span><span class="sxs-lookup"><span data-stu-id="c91ba-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="c91ba-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c91ba-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c91ba-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c91ba-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c91ba-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="c91ba-203">已為 PSNetworkInterface 新增 HostedWorkloads 屬性</span><span class="sxs-lookup"><span data-stu-id="c91ba-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="c91ba-204">已為以下功能新增 Cmdlet：由 ARM 支援的 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="c91ba-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="c91ba-205">已新增 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c91ba-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="c91ba-206">已新增 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c91ba-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="c91ba-207">已新增 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c91ba-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="c91ba-208">已新增 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c91ba-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="c91ba-209">已新增 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c91ba-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="c91ba-210">已新增 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c91ba-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="c91ba-211">已新增 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c91ba-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="c91ba-212">已新增 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c91ba-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="c91ba-213">已新增 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c91ba-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="c91ba-214">已新增 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c91ba-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="c91ba-215">已在應用程式閘道中新增受信任根憑證和自動調整組態的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="c91ba-216">已新增的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c91ba-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="c91ba-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c91ba-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c91ba-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c91ba-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c91ba-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c91ba-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c91ba-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c91ba-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c91ba-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="c91ba-226">已使用選擇性參數 TrustedRootCertificate 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="c91ba-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c91ba-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c91ba-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c91ba-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c91ba-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c91ba-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="c91ba-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c91ba-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="c91ba-231">已使用選擇性參數 AutoscaleConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="c91ba-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c91ba-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c91ba-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c91ba-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="c91ba-234">為介面端點 Get-AzureInterfaceEndpoint 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="c91ba-235">已在子網路中新增多個位址前置詞的支援。</span><span class="sxs-lookup"><span data-stu-id="c91ba-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="c91ba-236">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c91ba-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="c91ba-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c91ba-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c91ba-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c91ba-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c91ba-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="c91ba-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c91ba-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c91ba-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c91ba-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c91ba-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c91ba-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c91ba-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c91ba-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c91ba-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c91ba-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c91ba-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c91ba-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c91ba-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c91ba-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c91ba-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="c91ba-256">為子網路委派新增 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="c91ba-257">New-AzureRmDelegation：建立可新增至子網路的新委派</span><span class="sxs-lookup"><span data-stu-id="c91ba-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="c91ba-258">Remove-AzureRmDelegation：用於子網路，可從該子網路中移除提供的委派名稱</span><span class="sxs-lookup"><span data-stu-id="c91ba-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="c91ba-259">Add-AzureRmDelegation：用於子網路，可將提供的服務名稱新增為該子網路的委派</span><span class="sxs-lookup"><span data-stu-id="c91ba-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="c91ba-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="c91ba-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="c91ba-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="c91ba-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c91ba-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c91ba-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c91ba-263">支援受控磁碟</span><span class="sxs-lookup"><span data-stu-id="c91ba-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c91ba-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c91ba-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c91ba-265">已更新深入解析相依性。</span><span class="sxs-lookup"><span data-stu-id="c91ba-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-266">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-267">使用新參數 RollbackAction 更新 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c91ba-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="c91ba-268">使用新參數新增 OnErrorDeployment 的支援。</span><span class="sxs-lookup"><span data-stu-id="c91ba-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="c91ba-269">支援原則指派上的受控識別。</span><span class="sxs-lookup"><span data-stu-id="c91ba-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="c91ba-270">以 'New-AzureRmPolicyAssignment' 指派原則時不再需要具有預設值的參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="c91ba-271">新增 Get-AzureRmPolicyAlias Cmdlet 來擷取原則別名</span><span class="sxs-lookup"><span data-stu-id="c91ba-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c91ba-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c91ba-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c91ba-273">已修正問題 #7161</span><span class="sxs-lookup"><span data-stu-id="c91ba-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="c91ba-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="c91ba-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="c91ba-275">將 SKU 名稱更新為 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="c91ba-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="c91ba-276">將版本欄位新增至 PSSignalRResource 物件，以及將連接字串新增至 PSSignalRKeys 物件。</span><span class="sxs-lookup"><span data-stu-id="c91ba-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c91ba-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-277">AzureRM.Storage</span></span>
* <span data-ttu-id="c91ba-278">在 AzureRm.Storage 中支援不變原則</span><span class="sxs-lookup"><span data-stu-id="c91ba-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="c91ba-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c91ba-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="c91ba-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c91ba-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c91ba-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c91ba-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c91ba-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c91ba-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c91ba-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c91ba-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c91ba-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c91ba-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c91ba-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c91ba-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c91ba-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c91ba-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c91ba-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c91ba-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c91ba-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c91ba-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c91ba-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c91ba-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c91ba-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c91ba-290">AzureRM.Websites</span></span>
* <span data-ttu-id="c91ba-291">已新增兩個 Cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c91ba-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="c91ba-292">New-AzureRmAppServicePlan - 已新增 HyperV 切換以使用 Windows 容器建立 App Service 方案</span><span class="sxs-lookup"><span data-stu-id="c91ba-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="c91ba-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 已新增參數 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) 來建立和管理 Windows 容器應用程式</span><span class="sxs-lookup"><span data-stu-id="c91ba-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="c91ba-294">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c91ba-295">一般</span><span class="sxs-lookup"><span data-stu-id="c91ba-295">General</span></span>
* <span data-ttu-id="c91ba-296">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c91ba-297">已更新通用執行階段組件</span><span class="sxs-lookup"><span data-stu-id="c91ba-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c91ba-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c91ba-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c91ba-299">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c91ba-300">已修正的問題 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="c91ba-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="c91ba-301">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlets 目前處理相對路徑</span><span class="sxs-lookup"><span data-stu-id="c91ba-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="c91ba-302">已修正的問題 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="c91ba-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="c91ba-303">CertificateInformation 為可設定的屬性，允許 Set-AzureRmApiManagement Cmdlet 正常運作。</span><span class="sxs-lookup"><span data-stu-id="c91ba-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="c91ba-304">已藉由升級至 4.0.4-preview NuGet 而修正</span><span class="sxs-lookup"><span data-stu-id="c91ba-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="c91ba-305">已修正的問題 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="c91ba-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="c91ba-306">已修正依產品名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="c91ba-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="c91ba-307">已修正的問題 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="c91ba-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="c91ba-308">已修正依 API 名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="c91ba-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="c91ba-309">已新增對 AzureMonitor 記錄器的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-310">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-311">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c91ba-312">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c91ba-313">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c91ba-314">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="c91ba-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-315">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-316">已將預設的 Cmdlet 輸出表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="c91ba-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c91ba-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c91ba-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c91ba-318">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="c91ba-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="c91ba-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-319">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-320">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c91ba-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c91ba-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c91ba-322">已修正的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c91ba-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c91ba-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c91ba-324">已新增對 MultiValue 路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c91ba-325">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c91ba-326">已新增對子網路路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c91ba-327">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="c91ba-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c91ba-328">已新增對設定檔中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c91ba-329">已新增對設定檔中預期狀態碼的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c91ba-330">已新增對端點中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="c91ba-331">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c91ba-332">一般</span><span class="sxs-lookup"><span data-stu-id="c91ba-332">General</span></span>
* <span data-ttu-id="c91ba-333">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-334">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-335">已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖</span><span class="sxs-lookup"><span data-stu-id="c91ba-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-336">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-337">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c91ba-338">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c91ba-339">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="c91ba-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c91ba-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c91ba-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="c91ba-341">修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-342">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-343">已將預設模式表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="c91ba-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c91ba-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c91ba-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c91ba-345">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="c91ba-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-346">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-347">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c91ba-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c91ba-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c91ba-349">修正問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c91ba-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c91ba-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c91ba-351">支援 MultiValue 路由方法</span><span class="sxs-lookup"><span data-stu-id="c91ba-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c91ba-352">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c91ba-353">支援子網路路由方法</span><span class="sxs-lookup"><span data-stu-id="c91ba-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c91ba-354">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="c91ba-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c91ba-355">支援設定檔中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="c91ba-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c91ba-356">支援設定檔中的預期狀態碼</span><span class="sxs-lookup"><span data-stu-id="c91ba-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c91ba-357">支援端點中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="c91ba-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c91ba-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c91ba-358">AzureRM.Websites</span></span>
* <span data-ttu-id="c91ba-359">已修正未正確設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="c91ba-360">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-361">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-362">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c91ba-363">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="c91ba-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="c91ba-364">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="c91ba-365">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="c91ba-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-366">Azure.Storage</span></span>
* <span data-ttu-id="c91ba-367">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="c91ba-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="c91ba-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c91ba-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c91ba-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c91ba-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c91ba-370">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="c91ba-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c91ba-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="c91ba-372">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c91ba-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c91ba-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c91ba-374">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="c91ba-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c91ba-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="c91ba-376">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c91ba-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c91ba-377">AzureRM.Automation</span></span>
* <span data-ttu-id="c91ba-378">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c91ba-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c91ba-379">AzureRM.Backup</span></span>
* <span data-ttu-id="c91ba-380">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c91ba-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c91ba-381">AzureRM.Batch</span></span>
* <span data-ttu-id="c91ba-382">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="c91ba-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="c91ba-383">AzureRM.Billing</span></span>
* <span data-ttu-id="c91ba-384">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c91ba-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c91ba-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="c91ba-386">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c91ba-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c91ba-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c91ba-388">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-389">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-390">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c91ba-391">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="c91ba-392">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="c91ba-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="c91ba-393">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="c91ba-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c91ba-394">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c91ba-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c91ba-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="c91ba-396">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c91ba-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c91ba-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c91ba-398">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="c91ba-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c91ba-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="c91ba-400">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="c91ba-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c91ba-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="c91ba-402">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c91ba-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c91ba-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c91ba-404">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c91ba-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c91ba-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c91ba-406">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c91ba-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c91ba-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c91ba-408">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="c91ba-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="c91ba-409">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c91ba-410">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c91ba-411">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="c91ba-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c91ba-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="c91ba-413">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c91ba-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c91ba-414">AzureRM.Dns</span></span>
* <span data-ttu-id="c91ba-415">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c91ba-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c91ba-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c91ba-417">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c91ba-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c91ba-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="c91ba-419">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="c91ba-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c91ba-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="c91ba-421">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c91ba-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c91ba-422">AzureRM.Insights</span></span>
* <span data-ttu-id="c91ba-423">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c91ba-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c91ba-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="c91ba-425">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c91ba-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c91ba-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c91ba-427">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c91ba-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c91ba-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c91ba-429">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="c91ba-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c91ba-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="c91ba-431">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="c91ba-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c91ba-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="c91ba-433">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="c91ba-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c91ba-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="c91ba-435">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="c91ba-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="c91ba-436">AzureRM.Media</span></span>
* <span data-ttu-id="c91ba-437">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-438">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-439">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="c91ba-440">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="c91ba-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c91ba-441">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="c91ba-442">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c91ba-443">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c91ba-444">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c91ba-445">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="c91ba-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="c91ba-446">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="c91ba-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="c91ba-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c91ba-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="c91ba-448">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c91ba-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c91ba-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c91ba-450">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c91ba-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c91ba-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c91ba-452">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c91ba-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c91ba-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c91ba-454">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="c91ba-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c91ba-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="c91ba-456">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c91ba-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c91ba-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c91ba-458">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="c91ba-459">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="c91ba-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="c91ba-460">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="c91ba-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="c91ba-461">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c91ba-462">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="c91ba-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="c91ba-463">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c91ba-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c91ba-464">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="c91ba-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c91ba-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c91ba-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c91ba-466">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c91ba-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c91ba-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c91ba-468">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c91ba-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c91ba-469">AzureRM.Relay</span></span>
* <span data-ttu-id="c91ba-470">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-471">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-472">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="c91ba-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="c91ba-473">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c91ba-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="c91ba-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c91ba-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="c91ba-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c91ba-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="c91ba-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c91ba-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="c91ba-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c91ba-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="c91ba-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c91ba-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="c91ba-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c91ba-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="c91ba-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c91ba-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="c91ba-481">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="c91ba-482">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="c91ba-483">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c91ba-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c91ba-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c91ba-485">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c91ba-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c91ba-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c91ba-487">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c91ba-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c91ba-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c91ba-489">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c91ba-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c91ba-490">AzureRM.Sql</span></span>
* <span data-ttu-id="c91ba-491">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c91ba-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-492">AzureRM.Storage</span></span>
* <span data-ttu-id="c91ba-493">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="c91ba-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="c91ba-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="c91ba-495">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c91ba-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c91ba-496">AzureRM.Tags</span></span>
* <span data-ttu-id="c91ba-497">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c91ba-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c91ba-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c91ba-499">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="c91ba-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="c91ba-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="c91ba-501">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c91ba-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c91ba-502">AzureRM.Websites</span></span>
* <span data-ttu-id="c91ba-503">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="c91ba-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="c91ba-504">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c91ba-505">一般</span><span class="sxs-lookup"><span data-stu-id="c91ba-505">General</span></span>
* <span data-ttu-id="c91ba-506">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="c91ba-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-507">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-508">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="c91ba-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="c91ba-509">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c91ba-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-510">Azure.Storage</span></span>
* <span data-ttu-id="c91ba-511">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="c91ba-512">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="c91ba-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c91ba-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c91ba-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c91ba-514">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="c91ba-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="c91ba-515">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="c91ba-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="c91ba-516">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="c91ba-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="c91ba-517">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="c91ba-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="c91ba-518">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="c91ba-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="c91ba-519">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="c91ba-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-520">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-521">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="c91ba-522">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="c91ba-523">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="c91ba-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="c91ba-524">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="c91ba-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="c91ba-525">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="c91ba-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="c91ba-526">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="c91ba-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="c91ba-527">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="c91ba-528">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="c91ba-529">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="c91ba-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="c91ba-530">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="c91ba-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c91ba-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c91ba-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c91ba-532">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="c91ba-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="c91ba-533">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="c91ba-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="c91ba-534">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="c91ba-535">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c91ba-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c91ba-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c91ba-537">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="c91ba-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c91ba-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c91ba-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="c91ba-539">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="c91ba-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c91ba-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c91ba-540">AzureRM.Insights</span></span>
* <span data-ttu-id="c91ba-541">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="c91ba-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="c91ba-542">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="c91ba-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c91ba-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c91ba-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c91ba-544">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-545">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-546">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="c91ba-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-547">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-548">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="c91ba-549">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="c91ba-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c91ba-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c91ba-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c91ba-551">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="c91ba-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="c91ba-552">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="c91ba-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c91ba-553">AzureRM.Sql</span></span>
* <span data-ttu-id="c91ba-554">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="c91ba-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="c91ba-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c91ba-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c91ba-556">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="c91ba-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="c91ba-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="c91ba-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="c91ba-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="c91ba-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="c91ba-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="c91ba-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="c91ba-560">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="c91ba-561">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="c91ba-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c91ba-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-562">AzureRM.Storage</span></span>
* <span data-ttu-id="c91ba-563">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="c91ba-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="c91ba-564">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="c91ba-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="c91ba-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c91ba-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c91ba-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c91ba-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c91ba-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c91ba-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c91ba-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c91ba-568">AzureRM.Tags</span></span>
* <span data-ttu-id="c91ba-569">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="c91ba-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="c91ba-570">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-571">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-572">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="c91ba-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c91ba-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-573">Azure.Storage</span></span>
* <span data-ttu-id="c91ba-574">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="c91ba-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="c91ba-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c91ba-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="c91ba-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c91ba-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c91ba-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c91ba-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c91ba-578">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="c91ba-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c91ba-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c91ba-579">AzureRM.Automation</span></span>
* <span data-ttu-id="c91ba-580">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-581">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-582">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c91ba-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="c91ba-583">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c91ba-584">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c91ba-585">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="c91ba-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="c91ba-586">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="c91ba-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c91ba-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c91ba-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="c91ba-588">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="c91ba-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c91ba-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c91ba-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c91ba-590">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="c91ba-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c91ba-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c91ba-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c91ba-592">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="c91ba-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-593">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-594">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="c91ba-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="c91ba-595">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="c91ba-596">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="c91ba-597">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c91ba-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="c91ba-598">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c91ba-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="c91ba-599">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c91ba-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c91ba-600">AzureRM.Relay</span></span>
* <span data-ttu-id="c91ba-601">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-602">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-603">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c91ba-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="c91ba-604">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="c91ba-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="c91ba-605">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="c91ba-606">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="c91ba-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="c91ba-607">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c91ba-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c91ba-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c91ba-609">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="c91ba-610">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c91ba-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="c91ba-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c91ba-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c91ba-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c91ba-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c91ba-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c91ba-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c91ba-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c91ba-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c91ba-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c91ba-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="c91ba-616">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="c91ba-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c91ba-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c91ba-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c91ba-618">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c91ba-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c91ba-619">AzureRM.Sql</span></span>
* <span data-ttu-id="c91ba-620">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="c91ba-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="c91ba-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="c91ba-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c91ba-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c91ba-623">AzureRM.Websites</span></span>
* <span data-ttu-id="c91ba-624">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="c91ba-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="c91ba-625">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="c91ba-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="c91ba-626">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="c91ba-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="c91ba-627">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c91ba-628">一般</span><span class="sxs-lookup"><span data-stu-id="c91ba-628">General</span></span>
* <span data-ttu-id="c91ba-629">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="c91ba-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-630">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-631">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="c91ba-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-632">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-633">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="c91ba-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="c91ba-634">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="c91ba-635">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c91ba-636">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="c91ba-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="c91ba-637">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c91ba-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="c91ba-638">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="c91ba-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="c91ba-639">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c91ba-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c91ba-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c91ba-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c91ba-641">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="c91ba-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="c91ba-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c91ba-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c91ba-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c91ba-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c91ba-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c91ba-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c91ba-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c91ba-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c91ba-646">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="c91ba-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c91ba-647">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c91ba-648">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="c91ba-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="c91ba-649">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="c91ba-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c91ba-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c91ba-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="c91ba-651">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c91ba-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="c91ba-652">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="c91ba-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="c91ba-653">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="c91ba-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="c91ba-654">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="c91ba-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c91ba-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c91ba-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c91ba-656">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-657">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-658">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="c91ba-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="c91ba-659">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="c91ba-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="c91ba-660">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c91ba-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c91ba-661">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c91ba-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c91ba-662">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c91ba-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c91ba-663">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c91ba-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c91ba-664">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c91ba-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c91ba-665">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c91ba-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c91ba-666">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c91ba-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c91ba-667">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c91ba-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c91ba-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c91ba-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c91ba-669">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="c91ba-670">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="c91ba-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="c91ba-671">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c91ba-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-672">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-673">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="c91ba-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="c91ba-674">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="c91ba-675">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="c91ba-676">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="c91ba-677">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="c91ba-678">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="c91ba-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c91ba-679">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="c91ba-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c91ba-680">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="c91ba-681">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="c91ba-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c91ba-682">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="c91ba-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c91ba-683">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="c91ba-684">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="c91ba-685">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="c91ba-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c91ba-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c91ba-687">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="c91ba-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c91ba-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c91ba-688">AzureRM.Sql</span></span>
* <span data-ttu-id="c91ba-689">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="c91ba-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="c91ba-690">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="c91ba-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="c91ba-691">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-692">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-693">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="c91ba-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="c91ba-694">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="c91ba-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c91ba-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c91ba-695">Azure.Storage</span></span>
* <span data-ttu-id="c91ba-696">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="c91ba-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-697">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-698">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="c91ba-699">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="c91ba-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c91ba-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c91ba-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c91ba-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c91ba-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c91ba-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c91ba-703">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="c91ba-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="c91ba-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c91ba-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="c91ba-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c91ba-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="c91ba-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c91ba-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="c91ba-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c91ba-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="c91ba-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="c91ba-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="c91ba-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c91ba-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="c91ba-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c91ba-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="c91ba-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c91ba-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="c91ba-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c91ba-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="c91ba-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c91ba-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="c91ba-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c91ba-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="c91ba-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c91ba-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="c91ba-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c91ba-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="c91ba-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c91ba-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c91ba-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c91ba-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="c91ba-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c91ba-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c91ba-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c91ba-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="c91ba-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c91ba-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="c91ba-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c91ba-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c91ba-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c91ba-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c91ba-724">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="c91ba-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c91ba-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c91ba-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c91ba-726">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="c91ba-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c91ba-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c91ba-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c91ba-728">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="c91ba-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="c91ba-729">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="c91ba-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="c91ba-730">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="c91ba-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c91ba-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c91ba-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c91ba-732">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="c91ba-733">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c91ba-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c91ba-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c91ba-734">AzureRM.Sql</span></span>
* <span data-ttu-id="c91ba-735">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c91ba-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c91ba-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c91ba-737">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c91ba-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c91ba-738">AzureRM.Websites</span></span>
* <span data-ttu-id="c91ba-739">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="c91ba-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="c91ba-740">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="c91ba-741">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="c91ba-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c91ba-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c91ba-743">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="c91ba-744">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-745">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-746">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="c91ba-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c91ba-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c91ba-747">AzureRM.Compute</span></span>
* <span data-ttu-id="c91ba-748">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="c91ba-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="c91ba-749">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="c91ba-750">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="c91ba-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c91ba-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c91ba-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c91ba-752">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="c91ba-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="c91ba-753">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="c91ba-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="c91ba-754">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="c91ba-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="c91ba-755">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="c91ba-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="c91ba-756">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="c91ba-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="c91ba-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c91ba-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c91ba-758">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="c91ba-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-759">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-760">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="c91ba-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c91ba-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c91ba-761">AzureRM.Resources</span></span>
* <span data-ttu-id="c91ba-762">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c91ba-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c91ba-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c91ba-764">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="c91ba-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c91ba-765">AzureRM.Sql</span></span>
* <span data-ttu-id="c91ba-766">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c91ba-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="c91ba-767">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c91ba-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c91ba-768">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c91ba-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c91ba-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c91ba-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c91ba-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c91ba-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c91ba-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c91ba-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c91ba-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c91ba-772">AzureRM.Websites</span></span>
* <span data-ttu-id="c91ba-773">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="c91ba-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="c91ba-774">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="c91ba-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c91ba-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c91ba-775">AzureRM.Profile</span></span>
* <span data-ttu-id="c91ba-776">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="c91ba-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c91ba-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c91ba-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c91ba-778">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="c91ba-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c91ba-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c91ba-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c91ba-780">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="c91ba-781">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="c91ba-782">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="c91ba-783">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="c91ba-784">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="c91ba-785">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="c91ba-786">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="c91ba-786">Added support for MSI identity</span></span>
* <span data-ttu-id="c91ba-787">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="c91ba-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="c91ba-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c91ba-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="c91ba-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="c91ba-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c91ba-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="c91ba-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c91ba-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c91ba-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c91ba-792">AzureRM.Batch</span></span>
* <span data-ttu-id="c91ba-793">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="c91ba-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="c91ba-794">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="c91ba-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c91ba-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c91ba-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="c91ba-796">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="c91ba-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c91ba-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c91ba-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c91ba-798">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="c91ba-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c91ba-799">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="c91ba-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="c91ba-800">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="c91ba-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="c91ba-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c91ba-801">AzureRM.Network</span></span>
* <span data-ttu-id="c91ba-802">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="c91ba-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="c91ba-803">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="c91ba-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="c91ba-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c91ba-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="c91ba-805">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="c91ba-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="c91ba-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c91ba-807">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="c91ba-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="c91ba-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c91ba-809">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="c91ba-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="c91ba-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c91ba-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c91ba-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c91ba-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c91ba-812">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="c91ba-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c91ba-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c91ba-813">AzureRM.Sql</span></span>
* <span data-ttu-id="c91ba-814">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="c91ba-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="c91ba-815">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="c91ba-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="c91ba-816">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="c91ba-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="c91ba-817">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="c91ba-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="c91ba-818">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="c91ba-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="c91ba-819">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c91ba-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c91ba-820">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c91ba-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c91ba-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c91ba-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c91ba-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c91ba-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c91ba-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c91ba-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c91ba-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c91ba-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c91ba-825">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="c91ba-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
