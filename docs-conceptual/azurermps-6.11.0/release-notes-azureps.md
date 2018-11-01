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
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/01/2018
ms.locfileid: "50738099"
---
# <a name="release-notes"></a><span data-ttu-id="07ca3-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="07ca3-103">Release notes</span></span>

<span data-ttu-id="07ca3-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="07ca3-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="07ca3-105">6.11.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-106">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-107">修正 CloudShell 中 Get-AzureRmSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="07ca3-108">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="07ca3-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="07ca3-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="07ca3-109">AzureRM.Backup</span></span>
* <span data-ttu-id="07ca3-110">淘汰的 Azure 備份 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-111">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-112">已將新的大小新增至虛擬機器大小白名單，當使用 'New-AzureRmVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="07ca3-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="07ca3-113">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="07ca3-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07ca3-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="07ca3-115">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="07ca3-116">Get-AzureRmDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="07ca3-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="07ca3-117">Add-AzureRmDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="07ca3-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="07ca3-118">Set-AzureRmDataLakeStoreVirtualNetworkRule：在指定的 Data Lake Store 帳戶中修改指定的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="07ca3-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="07ca3-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="07ca3-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-120">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-121">更新 Cmdlet Test-AzureRmNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="07ca3-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="07ca3-122">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-123">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-124">修正當 Get-AzureRMRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="07ca3-125">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="07ca3-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="07ca3-126">6.10.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="07ca3-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-127">Azure.Storage</span></span>
* <span data-ttu-id="07ca3-128">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="07ca3-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="07ca3-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="07ca3-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="07ca3-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="07ca3-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07ca3-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="07ca3-132">在沒有現有帳戶的情況下支援 Get-AzureRmCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="07ca3-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-133">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-134">修正 Get-AzureRmVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="07ca3-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="07ca3-135">已將 'SimpleParameterSet' 的範例新增到 New-AzureRmVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="07ca3-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="07ca3-136">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="07ca3-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="07ca3-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="07ca3-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="07ca3-138">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="07ca3-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-139">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-140">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="07ca3-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="07ca3-141">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-141">new cmdlets added</span></span>
    - <span data-ttu-id="07ca3-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="07ca3-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="07ca3-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="07ca3-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="07ca3-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="07ca3-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="07ca3-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="07ca3-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="07ca3-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="07ca3-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="07ca3-148">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="07ca3-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="07ca3-149">已新增 New-AzureRmVirtualNetworkTap、Get-AzureRmVirtualNetworkTap、Set-AzureRmVirtualNetworkTap 和 Remove-AzureRmVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="07ca3-150">已新增 Set-AzureRmNEtworkInterfaceTapConfig、Get-AzureRmNEtworkInterfaceTapConfig 和 Remove-AzureRmNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="07ca3-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="07ca3-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="07ca3-152">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="07ca3-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="07ca3-153">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="07ca3-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-154">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-155">將遺漏的 -Mode 參數新增至 Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="07ca3-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="07ca3-156">修正 Get-AzureRmProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="07ca3-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="07ca3-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="07ca3-157">AzureRM.Sql</span></span>
* <span data-ttu-id="07ca3-158">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="07ca3-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-159">AzureRM.Storage</span></span>
* <span data-ttu-id="07ca3-160">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="07ca3-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="07ca3-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="07ca3-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="07ca3-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="07ca3-162">AzureRM.Websites</span></span>
* <span data-ttu-id="07ca3-163">新 Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="07ca3-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="07ca3-164">新 Cmdlet New-AzureRMWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="07ca3-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="07ca3-165">6.9.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="07ca3-166">一般</span><span class="sxs-lookup"><span data-stu-id="07ca3-166">General</span></span>
* <span data-ttu-id="07ca3-167">已將 AzureRM.SignalR 新增至 AzureRM 彙總模組</span><span class="sxs-lookup"><span data-stu-id="07ca3-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-168">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-169">儲存體通用程式碼的小幅變更</span><span class="sxs-lookup"><span data-stu-id="07ca3-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="07ca3-170">已更新說明檔以包含完整的參數類型。</span><span class="sxs-lookup"><span data-stu-id="07ca3-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="07ca3-171">已變更 - 非強制性的 ServicePrincipal 位在 ServicePrincipalCertificateWithSubscriptionId 參數集</span><span class="sxs-lookup"><span data-stu-id="07ca3-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="07ca3-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-172">Azure.Storage</span></span>
* <span data-ttu-id="07ca3-173">支援使用 OAuth 建立儲存體內容。</span><span class="sxs-lookup"><span data-stu-id="07ca3-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="07ca3-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="07ca3-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="07ca3-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="07ca3-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="07ca3-176">已在 CDN 定價 SKU 中新增 Standard_Microsoft。</span><span class="sxs-lookup"><span data-stu-id="07ca3-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-177">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-178">將金鑰保存庫和儲存體上的相依性移至一般相依性</span><span class="sxs-lookup"><span data-stu-id="07ca3-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="07ca3-179">對 AEM Cmdlet 新增更多的虛擬機器大小支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="07ca3-180">將 PublicIPPrefix 參數新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="07ca3-181">將 ResourceId 參數新增至 Invoke-AzureRmVMRunCommand Cmdelt</span><span class="sxs-lookup"><span data-stu-id="07ca3-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="07ca3-182">新增 Invoke-AzureRmVmssVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="07ca3-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="07ca3-183">AzureRM.Dns</span></span>
* <span data-ttu-id="07ca3-184">已新增建立 DNS 記錄時的別名記錄支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="07ca3-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="07ca3-185">AzureRM.Insights</span></span>
* <span data-ttu-id="07ca3-186">已修正問題 #6833 和 #7102 (診斷設定區域)</span><span class="sxs-lookup"><span data-stu-id="07ca3-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="07ca3-187">建立和列出/取得診斷設定時的預設名稱問題 (例如 'service')</span><span class="sxs-lookup"><span data-stu-id="07ca3-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="07ca3-188">以類別建立診斷設定的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="07ca3-189">已新增計量時間粒紋參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="07ca3-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="07ca3-190">Timegrains 參數還是可用 (這是非中斷性變更)，但會在後端中遭到忽略，因為只有 PT1M 有效</span><span class="sxs-lookup"><span data-stu-id="07ca3-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-191">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-192">LoadBalancer Cmdlet 的變更</span><span class="sxs-lookup"><span data-stu-id="07ca3-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="07ca3-193">LoadBalancerInboundNatPoolConfig：已新增 IdleTimeoutInMinutes、EnableFloatingIp 和 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="07ca3-194">LoadBalancerInboundNatRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="07ca3-195">LoadBalancerRuleConfig：已新增 EnableTcpReset 參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="07ca3-196">LoadBalancerProbeConfig：已為 Protocol 參數新增 "Https" 值的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="07ca3-197">已為新 LoadBalancer 的子資源 OutboundRule 新增命令</span><span class="sxs-lookup"><span data-stu-id="07ca3-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="07ca3-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="07ca3-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="07ca3-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="07ca3-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="07ca3-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="07ca3-203">已為 PSNetworkInterface 新增 HostedWorkloads 屬性</span><span class="sxs-lookup"><span data-stu-id="07ca3-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="07ca3-204">已為以下功能新增 Cmdlet：由 ARM 支援的 Azure 防火牆</span><span class="sxs-lookup"><span data-stu-id="07ca3-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="07ca3-205">已新增 Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="07ca3-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="07ca3-206">已新增 Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="07ca3-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="07ca3-207">已新增 New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="07ca3-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="07ca3-208">已新增 Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="07ca3-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="07ca3-209">已新增 New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07ca3-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="07ca3-210">已新增 New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="07ca3-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="07ca3-211">已新增 New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07ca3-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="07ca3-212">已新增 New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="07ca3-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="07ca3-213">已新增 New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07ca3-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="07ca3-214">已新增 New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="07ca3-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="07ca3-215">已在應用程式閘道中新增受信任根憑證和自動調整組態的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="07ca3-216">已新增的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="07ca3-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="07ca3-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="07ca3-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="07ca3-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="07ca3-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="07ca3-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="07ca3-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="07ca3-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="07ca3-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="07ca3-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="07ca3-226">已使用選擇性參數 TrustedRootCertificate 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="07ca3-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07ca3-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="07ca3-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07ca3-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="07ca3-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="07ca3-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="07ca3-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="07ca3-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="07ca3-231">已使用選擇性參數 AutoscaleConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="07ca3-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07ca3-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="07ca3-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07ca3-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="07ca3-234">為介面端點 Get-AzureInterfaceEndpoint 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="07ca3-235">已在子網路中新增多個位址前置詞的支援。</span><span class="sxs-lookup"><span data-stu-id="07ca3-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="07ca3-236">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="07ca3-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="07ca3-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="07ca3-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="07ca3-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="07ca3-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="07ca3-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="07ca3-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="07ca3-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="07ca3-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="07ca3-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="07ca3-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="07ca3-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="07ca3-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="07ca3-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="07ca3-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="07ca3-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="07ca3-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="07ca3-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="07ca3-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="07ca3-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="07ca3-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="07ca3-256">為子網路委派新增 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="07ca3-257">New-AzureRmDelegation：建立可新增至子網路的新委派</span><span class="sxs-lookup"><span data-stu-id="07ca3-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="07ca3-258">Remove-AzureRmDelegation：用於子網路，可從該子網路中移除提供的委派名稱</span><span class="sxs-lookup"><span data-stu-id="07ca3-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="07ca3-259">Add-AzureRmDelegation：用於子網路，可將提供的服務名稱新增為該子網路的委派</span><span class="sxs-lookup"><span data-stu-id="07ca3-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="07ca3-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="07ca3-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="07ca3-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="07ca3-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="07ca3-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="07ca3-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="07ca3-263">支援受控磁碟</span><span class="sxs-lookup"><span data-stu-id="07ca3-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="07ca3-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="07ca3-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="07ca3-265">已更新深入解析相依性。</span><span class="sxs-lookup"><span data-stu-id="07ca3-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-266">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-267">使用新參數 RollbackAction 更新 New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="07ca3-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="07ca3-268">使用新參數新增 OnErrorDeployment 的支援。</span><span class="sxs-lookup"><span data-stu-id="07ca3-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="07ca3-269">支援原則指派上的受控識別。</span><span class="sxs-lookup"><span data-stu-id="07ca3-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="07ca3-270">以 'New-AzureRmPolicyAssignment' 指派原則時不再需要具有預設值的參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="07ca3-271">新增 Get-AzureRmPolicyAlias Cmdlet 來擷取原則別名</span><span class="sxs-lookup"><span data-stu-id="07ca3-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="07ca3-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07ca3-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="07ca3-273">已修正問題 #7161</span><span class="sxs-lookup"><span data-stu-id="07ca3-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="07ca3-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="07ca3-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="07ca3-275">將 SKU 名稱更新為 Free_F1 和 Standard_S1</span><span class="sxs-lookup"><span data-stu-id="07ca3-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="07ca3-276">將版本欄位新增至 PSSignalRResource 物件，以及將連接字串新增至 PSSignalRKeys 物件。</span><span class="sxs-lookup"><span data-stu-id="07ca3-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="07ca3-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-277">AzureRM.Storage</span></span>
* <span data-ttu-id="07ca3-278">在 AzureRm.Storage 中支援不變原則</span><span class="sxs-lookup"><span data-stu-id="07ca3-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="07ca3-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="07ca3-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="07ca3-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="07ca3-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="07ca3-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="07ca3-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="07ca3-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="07ca3-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="07ca3-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="07ca3-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="07ca3-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="07ca3-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="07ca3-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="07ca3-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="07ca3-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="07ca3-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="07ca3-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="07ca3-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="07ca3-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="07ca3-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="07ca3-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="07ca3-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="07ca3-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="07ca3-290">AzureRM.Websites</span></span>
* <span data-ttu-id="07ca3-291">已新增兩個 Cmdlet：Get-AzureRmDeletedWebApp 和 Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="07ca3-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="07ca3-292">New-AzureRmAppServicePlan - 已新增 HyperV 切換以使用 Windows 容器建立 App Service 方案</span><span class="sxs-lookup"><span data-stu-id="07ca3-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="07ca3-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - 已新增參數 (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) 來建立和管理 Windows 容器應用程式</span><span class="sxs-lookup"><span data-stu-id="07ca3-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="07ca3-294">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="07ca3-295">一般</span><span class="sxs-lookup"><span data-stu-id="07ca3-295">General</span></span>
* <span data-ttu-id="07ca3-296">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="07ca3-297">已更新通用執行階段組件</span><span class="sxs-lookup"><span data-stu-id="07ca3-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="07ca3-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07ca3-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="07ca3-299">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="07ca3-300">已修正的問題 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="07ca3-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="07ca3-301">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlets 目前處理相對路徑</span><span class="sxs-lookup"><span data-stu-id="07ca3-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="07ca3-302">已修正的問題 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="07ca3-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="07ca3-303">CertificateInformation 為可設定的屬性，允許 Set-AzureRmApiManagement Cmdlet 正常運作。</span><span class="sxs-lookup"><span data-stu-id="07ca3-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="07ca3-304">已藉由升級至 4.0.4-preview NuGet 而修正</span><span class="sxs-lookup"><span data-stu-id="07ca3-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="07ca3-305">已修正的問題 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="07ca3-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="07ca3-306">已修正依產品名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="07ca3-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="07ca3-307">已修正的問題 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="07ca3-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="07ca3-308">已修正依 API 名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="07ca3-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="07ca3-309">已新增對 AzureMonitor 記錄器的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-310">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-311">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="07ca3-312">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="07ca3-313">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="07ca3-314">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="07ca3-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-315">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-316">已將預設的 Cmdlet 輸出表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="07ca3-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="07ca3-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="07ca3-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="07ca3-318">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="07ca3-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="07ca3-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-319">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-320">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="07ca3-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07ca3-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="07ca3-322">已修正的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="07ca3-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="07ca3-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="07ca3-324">已新增對 MultiValue 路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="07ca3-325">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="07ca3-326">已新增對子網路路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="07ca3-327">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="07ca3-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="07ca3-328">已新增對設定檔中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="07ca3-329">已新增對設定檔中預期狀態碼的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="07ca3-330">已新增對端點中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="07ca3-331">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="07ca3-332">一般</span><span class="sxs-lookup"><span data-stu-id="07ca3-332">General</span></span>
* <span data-ttu-id="07ca3-333">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-334">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-335">已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖</span><span class="sxs-lookup"><span data-stu-id="07ca3-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-336">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-337">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="07ca3-338">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="07ca3-339">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="07ca3-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="07ca3-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="07ca3-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="07ca3-341">修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-342">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-343">已將預設模式表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="07ca3-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="07ca3-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="07ca3-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="07ca3-345">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="07ca3-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-346">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-347">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="07ca3-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07ca3-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="07ca3-349">修正問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="07ca3-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="07ca3-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="07ca3-351">支援 MultiValue 路由方法</span><span class="sxs-lookup"><span data-stu-id="07ca3-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="07ca3-352">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="07ca3-353">支援子網路路由方法</span><span class="sxs-lookup"><span data-stu-id="07ca3-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="07ca3-354">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="07ca3-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="07ca3-355">支援設定檔中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="07ca3-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="07ca3-356">支援設定檔中的預期狀態碼</span><span class="sxs-lookup"><span data-stu-id="07ca3-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="07ca3-357">支援端點中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="07ca3-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="07ca3-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="07ca3-358">AzureRM.Websites</span></span>
* <span data-ttu-id="07ca3-359">已修正未正確設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="07ca3-360">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-361">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-362">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="07ca3-363">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="07ca3-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="07ca3-364">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="07ca3-365">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="07ca3-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-366">Azure.Storage</span></span>
* <span data-ttu-id="07ca3-367">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="07ca3-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="07ca3-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="07ca3-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="07ca3-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="07ca3-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="07ca3-370">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="07ca3-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="07ca3-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="07ca3-372">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="07ca3-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07ca3-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="07ca3-374">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="07ca3-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="07ca3-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="07ca3-376">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="07ca3-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="07ca3-377">AzureRM.Automation</span></span>
* <span data-ttu-id="07ca3-378">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="07ca3-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="07ca3-379">AzureRM.Backup</span></span>
* <span data-ttu-id="07ca3-380">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="07ca3-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="07ca3-381">AzureRM.Batch</span></span>
* <span data-ttu-id="07ca3-382">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="07ca3-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="07ca3-383">AzureRM.Billing</span></span>
* <span data-ttu-id="07ca3-384">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="07ca3-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="07ca3-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="07ca3-386">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="07ca3-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="07ca3-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="07ca3-388">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-389">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-390">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="07ca3-391">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="07ca3-392">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="07ca3-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="07ca3-393">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="07ca3-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="07ca3-394">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="07ca3-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="07ca3-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="07ca3-396">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="07ca3-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="07ca3-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="07ca3-398">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="07ca3-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="07ca3-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="07ca3-400">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="07ca3-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="07ca3-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="07ca3-402">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="07ca3-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="07ca3-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="07ca3-404">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="07ca3-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="07ca3-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="07ca3-406">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="07ca3-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07ca3-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="07ca3-408">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="07ca3-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="07ca3-409">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="07ca3-410">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="07ca3-411">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="07ca3-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="07ca3-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="07ca3-413">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="07ca3-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="07ca3-414">AzureRM.Dns</span></span>
* <span data-ttu-id="07ca3-415">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="07ca3-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="07ca3-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="07ca3-417">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="07ca3-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="07ca3-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="07ca3-419">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="07ca3-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="07ca3-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="07ca3-421">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="07ca3-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="07ca3-422">AzureRM.Insights</span></span>
* <span data-ttu-id="07ca3-423">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="07ca3-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="07ca3-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="07ca3-425">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="07ca3-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07ca3-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="07ca3-427">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="07ca3-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="07ca3-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="07ca3-429">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="07ca3-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="07ca3-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="07ca3-431">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="07ca3-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="07ca3-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="07ca3-433">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="07ca3-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="07ca3-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="07ca3-435">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="07ca3-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="07ca3-436">AzureRM.Media</span></span>
* <span data-ttu-id="07ca3-437">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-438">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-439">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="07ca3-440">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="07ca3-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="07ca3-441">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="07ca3-442">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="07ca3-443">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="07ca3-444">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="07ca3-445">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="07ca3-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="07ca3-446">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="07ca3-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="07ca3-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="07ca3-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="07ca3-448">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="07ca3-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07ca3-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="07ca3-450">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="07ca3-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="07ca3-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="07ca3-452">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="07ca3-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="07ca3-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="07ca3-454">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="07ca3-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="07ca3-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="07ca3-456">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="07ca3-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="07ca3-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="07ca3-458">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="07ca3-459">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="07ca3-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="07ca3-460">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="07ca3-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="07ca3-461">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="07ca3-462">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="07ca3-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="07ca3-463">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="07ca3-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="07ca3-464">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="07ca3-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="07ca3-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="07ca3-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="07ca3-466">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="07ca3-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="07ca3-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="07ca3-468">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="07ca3-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="07ca3-469">AzureRM.Relay</span></span>
* <span data-ttu-id="07ca3-470">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-471">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-472">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="07ca3-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="07ca3-473">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="07ca3-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="07ca3-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="07ca3-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="07ca3-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="07ca3-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="07ca3-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="07ca3-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="07ca3-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="07ca3-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="07ca3-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="07ca3-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="07ca3-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="07ca3-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="07ca3-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="07ca3-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="07ca3-481">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="07ca3-482">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="07ca3-483">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="07ca3-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="07ca3-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="07ca3-485">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="07ca3-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07ca3-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="07ca3-487">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="07ca3-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07ca3-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="07ca3-489">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="07ca3-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="07ca3-490">AzureRM.Sql</span></span>
* <span data-ttu-id="07ca3-491">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="07ca3-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-492">AzureRM.Storage</span></span>
* <span data-ttu-id="07ca3-493">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="07ca3-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="07ca3-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="07ca3-495">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="07ca3-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="07ca3-496">AzureRM.Tags</span></span>
* <span data-ttu-id="07ca3-497">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="07ca3-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="07ca3-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="07ca3-499">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="07ca3-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="07ca3-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="07ca3-501">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="07ca3-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="07ca3-502">AzureRM.Websites</span></span>
* <span data-ttu-id="07ca3-503">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="07ca3-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="07ca3-504">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="07ca3-505">一般</span><span class="sxs-lookup"><span data-stu-id="07ca3-505">General</span></span>
* <span data-ttu-id="07ca3-506">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="07ca3-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-507">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-508">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="07ca3-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="07ca3-509">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="07ca3-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-510">Azure.Storage</span></span>
* <span data-ttu-id="07ca3-511">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="07ca3-512">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="07ca3-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="07ca3-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07ca3-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="07ca3-514">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="07ca3-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="07ca3-515">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="07ca3-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="07ca3-516">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="07ca3-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="07ca3-517">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="07ca3-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="07ca3-518">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="07ca3-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="07ca3-519">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="07ca3-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-520">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-521">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="07ca3-522">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="07ca3-523">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="07ca3-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="07ca3-524">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="07ca3-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="07ca3-525">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="07ca3-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="07ca3-526">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="07ca3-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="07ca3-527">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="07ca3-528">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="07ca3-529">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="07ca3-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="07ca3-530">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="07ca3-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="07ca3-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="07ca3-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="07ca3-532">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="07ca3-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="07ca3-533">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="07ca3-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="07ca3-534">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="07ca3-535">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="07ca3-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07ca3-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="07ca3-537">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="07ca3-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="07ca3-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="07ca3-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="07ca3-539">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="07ca3-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="07ca3-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="07ca3-540">AzureRM.Insights</span></span>
* <span data-ttu-id="07ca3-541">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="07ca3-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="07ca3-542">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="07ca3-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="07ca3-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07ca3-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="07ca3-544">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-545">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-546">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="07ca3-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-547">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-548">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="07ca3-549">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="07ca3-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="07ca3-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07ca3-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="07ca3-551">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="07ca3-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="07ca3-552">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="07ca3-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="07ca3-553">AzureRM.Sql</span></span>
* <span data-ttu-id="07ca3-554">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="07ca3-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="07ca3-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="07ca3-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="07ca3-556">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="07ca3-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="07ca3-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="07ca3-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="07ca3-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="07ca3-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="07ca3-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="07ca3-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="07ca3-560">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="07ca3-561">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="07ca3-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="07ca3-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-562">AzureRM.Storage</span></span>
* <span data-ttu-id="07ca3-563">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="07ca3-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="07ca3-564">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="07ca3-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="07ca3-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07ca3-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="07ca3-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07ca3-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="07ca3-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07ca3-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="07ca3-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="07ca3-568">AzureRM.Tags</span></span>
* <span data-ttu-id="07ca3-569">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="07ca3-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="07ca3-570">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-571">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-572">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="07ca3-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="07ca3-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-573">Azure.Storage</span></span>
* <span data-ttu-id="07ca3-574">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="07ca3-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="07ca3-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="07ca3-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="07ca3-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="07ca3-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="07ca3-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="07ca3-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="07ca3-578">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="07ca3-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="07ca3-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="07ca3-579">AzureRM.Automation</span></span>
* <span data-ttu-id="07ca3-580">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-581">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-582">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07ca3-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="07ca3-583">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="07ca3-584">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="07ca3-585">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="07ca3-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="07ca3-586">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="07ca3-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="07ca3-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="07ca3-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="07ca3-588">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="07ca3-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="07ca3-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07ca3-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="07ca3-590">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="07ca3-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="07ca3-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="07ca3-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="07ca3-592">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="07ca3-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-593">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-594">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="07ca3-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="07ca3-595">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="07ca3-596">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="07ca3-597">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="07ca3-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="07ca3-598">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="07ca3-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="07ca3-599">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="07ca3-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="07ca3-600">AzureRM.Relay</span></span>
* <span data-ttu-id="07ca3-601">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-602">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-603">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="07ca3-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="07ca3-604">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="07ca3-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="07ca3-605">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="07ca3-606">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="07ca3-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="07ca3-607">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="07ca3-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07ca3-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="07ca3-609">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="07ca3-610">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="07ca3-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="07ca3-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="07ca3-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="07ca3-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="07ca3-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="07ca3-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="07ca3-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="07ca3-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="07ca3-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="07ca3-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="07ca3-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="07ca3-616">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="07ca3-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="07ca3-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07ca3-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="07ca3-618">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="07ca3-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="07ca3-619">AzureRM.Sql</span></span>
* <span data-ttu-id="07ca3-620">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="07ca3-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="07ca3-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="07ca3-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="07ca3-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="07ca3-623">AzureRM.Websites</span></span>
* <span data-ttu-id="07ca3-624">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="07ca3-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="07ca3-625">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="07ca3-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="07ca3-626">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="07ca3-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="07ca3-627">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="07ca3-628">一般</span><span class="sxs-lookup"><span data-stu-id="07ca3-628">General</span></span>
* <span data-ttu-id="07ca3-629">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="07ca3-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-630">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-631">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="07ca3-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-632">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-633">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="07ca3-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="07ca3-634">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="07ca3-635">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="07ca3-636">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="07ca3-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="07ca3-637">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="07ca3-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="07ca3-638">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="07ca3-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="07ca3-639">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="07ca3-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="07ca3-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="07ca3-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="07ca3-641">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="07ca3-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="07ca3-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="07ca3-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="07ca3-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="07ca3-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="07ca3-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="07ca3-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="07ca3-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07ca3-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="07ca3-646">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="07ca3-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="07ca3-647">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="07ca3-648">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="07ca3-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="07ca3-649">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="07ca3-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="07ca3-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="07ca3-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="07ca3-651">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="07ca3-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="07ca3-652">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="07ca3-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="07ca3-653">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="07ca3-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="07ca3-654">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="07ca3-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="07ca3-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07ca3-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="07ca3-656">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-657">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-658">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="07ca3-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="07ca3-659">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="07ca3-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="07ca3-660">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="07ca3-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="07ca3-661">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="07ca3-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="07ca3-662">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="07ca3-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="07ca3-663">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="07ca3-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="07ca3-664">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="07ca3-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="07ca3-665">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="07ca3-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="07ca3-666">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="07ca3-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="07ca3-667">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="07ca3-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="07ca3-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="07ca3-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="07ca3-669">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="07ca3-670">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="07ca3-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="07ca3-671">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="07ca3-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-672">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-673">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="07ca3-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="07ca3-674">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="07ca3-675">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="07ca3-676">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="07ca3-677">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="07ca3-678">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="07ca3-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="07ca3-679">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="07ca3-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="07ca3-680">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="07ca3-681">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="07ca3-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="07ca3-682">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="07ca3-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="07ca3-683">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="07ca3-684">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="07ca3-685">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="07ca3-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="07ca3-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="07ca3-687">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="07ca3-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="07ca3-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="07ca3-688">AzureRM.Sql</span></span>
* <span data-ttu-id="07ca3-689">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="07ca3-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="07ca3-690">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="07ca3-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="07ca3-691">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-692">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-693">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="07ca3-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="07ca3-694">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="07ca3-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="07ca3-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="07ca3-695">Azure.Storage</span></span>
* <span data-ttu-id="07ca3-696">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="07ca3-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-697">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-698">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="07ca3-699">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="07ca3-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="07ca3-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="07ca3-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="07ca3-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="07ca3-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="07ca3-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="07ca3-703">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="07ca3-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="07ca3-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="07ca3-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="07ca3-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="07ca3-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="07ca3-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="07ca3-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="07ca3-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="07ca3-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="07ca3-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="07ca3-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="07ca3-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="07ca3-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="07ca3-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="07ca3-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="07ca3-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="07ca3-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="07ca3-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="07ca3-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="07ca3-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="07ca3-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="07ca3-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="07ca3-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="07ca3-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="07ca3-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="07ca3-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="07ca3-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="07ca3-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="07ca3-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="07ca3-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="07ca3-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="07ca3-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="07ca3-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="07ca3-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="07ca3-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="07ca3-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="07ca3-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="07ca3-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="07ca3-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="07ca3-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="07ca3-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="07ca3-724">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="07ca3-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="07ca3-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07ca3-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="07ca3-726">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="07ca3-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="07ca3-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="07ca3-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="07ca3-728">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="07ca3-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="07ca3-729">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="07ca3-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="07ca3-730">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="07ca3-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="07ca3-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="07ca3-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="07ca3-732">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="07ca3-733">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07ca3-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="07ca3-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="07ca3-734">AzureRM.Sql</span></span>
* <span data-ttu-id="07ca3-735">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="07ca3-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="07ca3-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="07ca3-737">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="07ca3-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="07ca3-738">AzureRM.Websites</span></span>
* <span data-ttu-id="07ca3-739">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="07ca3-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="07ca3-740">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="07ca3-741">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="07ca3-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="07ca3-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="07ca3-743">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="07ca3-744">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-745">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-746">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="07ca3-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="07ca3-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="07ca3-747">AzureRM.Compute</span></span>
* <span data-ttu-id="07ca3-748">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="07ca3-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="07ca3-749">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="07ca3-750">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="07ca3-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="07ca3-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="07ca3-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="07ca3-752">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="07ca3-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="07ca3-753">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="07ca3-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="07ca3-754">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="07ca3-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="07ca3-755">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="07ca3-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="07ca3-756">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="07ca3-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="07ca3-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="07ca3-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="07ca3-758">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="07ca3-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-759">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-760">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="07ca3-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="07ca3-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="07ca3-761">AzureRM.Resources</span></span>
* <span data-ttu-id="07ca3-762">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="07ca3-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="07ca3-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="07ca3-764">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="07ca3-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="07ca3-765">AzureRM.Sql</span></span>
* <span data-ttu-id="07ca3-766">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07ca3-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="07ca3-767">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="07ca3-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="07ca3-768">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="07ca3-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="07ca3-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="07ca3-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="07ca3-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="07ca3-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="07ca3-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="07ca3-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="07ca3-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="07ca3-772">AzureRM.Websites</span></span>
* <span data-ttu-id="07ca3-773">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="07ca3-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="07ca3-774">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="07ca3-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="07ca3-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="07ca3-775">AzureRM.Profile</span></span>
* <span data-ttu-id="07ca3-776">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="07ca3-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="07ca3-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="07ca3-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="07ca3-778">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="07ca3-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="07ca3-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="07ca3-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="07ca3-780">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="07ca3-781">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="07ca3-782">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="07ca3-783">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="07ca3-784">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="07ca3-785">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="07ca3-786">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="07ca3-786">Added support for MSI identity</span></span>
* <span data-ttu-id="07ca3-787">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="07ca3-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="07ca3-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="07ca3-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="07ca3-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="07ca3-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="07ca3-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="07ca3-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="07ca3-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="07ca3-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="07ca3-792">AzureRM.Batch</span></span>
* <span data-ttu-id="07ca3-793">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="07ca3-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="07ca3-794">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="07ca3-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="07ca3-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="07ca3-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="07ca3-796">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="07ca3-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="07ca3-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="07ca3-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="07ca3-798">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="07ca3-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="07ca3-799">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="07ca3-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="07ca3-800">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="07ca3-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="07ca3-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="07ca3-801">AzureRM.Network</span></span>
* <span data-ttu-id="07ca3-802">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="07ca3-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="07ca3-803">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="07ca3-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="07ca3-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ca3-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="07ca3-805">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="07ca3-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="07ca3-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="07ca3-807">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="07ca3-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="07ca3-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="07ca3-809">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="07ca3-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="07ca3-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="07ca3-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="07ca3-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="07ca3-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="07ca3-812">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="07ca3-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="07ca3-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="07ca3-813">AzureRM.Sql</span></span>
* <span data-ttu-id="07ca3-814">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="07ca3-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="07ca3-815">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="07ca3-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="07ca3-816">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="07ca3-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="07ca3-817">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="07ca3-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="07ca3-818">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="07ca3-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="07ca3-819">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="07ca3-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="07ca3-820">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="07ca3-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="07ca3-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="07ca3-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="07ca3-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="07ca3-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="07ca3-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="07ca3-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="07ca3-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="07ca3-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="07ca3-825">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="07ca3-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
