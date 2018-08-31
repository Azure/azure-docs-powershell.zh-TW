---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250089"
---
# <a name="release-notes"></a><span data-ttu-id="81e66-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="81e66-103">Release notes</span></span>

<span data-ttu-id="81e66-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="81e66-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="81e66-105">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="81e66-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="81e66-106">一般</span><span class="sxs-lookup"><span data-stu-id="81e66-106">General</span></span>
* <span data-ttu-id="81e66-107">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="81e66-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="81e66-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="81e66-108">AzureRM.Profile</span></span>
* <span data-ttu-id="81e66-109">已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖</span><span class="sxs-lookup"><span data-stu-id="81e66-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="81e66-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="81e66-110">AzureRM.Compute</span></span>
* <span data-ttu-id="81e66-111">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="81e66-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="81e66-112">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="81e66-113">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="81e66-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="81e66-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="81e66-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="81e66-115">修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="81e66-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="81e66-116">AzureRM.Network</span></span>
* <span data-ttu-id="81e66-117">已將預設模式表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="81e66-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="81e66-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="81e66-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="81e66-119">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="81e66-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="81e66-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="81e66-120">AzureRM.Resources</span></span>
* <span data-ttu-id="81e66-121">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="81e66-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="81e66-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="81e66-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="81e66-123">修正問題</span><span class="sxs-lookup"><span data-stu-id="81e66-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="81e66-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="81e66-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="81e66-125">支援 MultiValue 路由方法</span><span class="sxs-lookup"><span data-stu-id="81e66-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="81e66-126">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="81e66-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="81e66-127">支援子網路路由方法</span><span class="sxs-lookup"><span data-stu-id="81e66-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="81e66-128">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="81e66-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="81e66-129">支援設定檔中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="81e66-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="81e66-130">支援設定檔中的預期狀態碼</span><span class="sxs-lookup"><span data-stu-id="81e66-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="81e66-131">支援端點中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="81e66-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="81e66-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="81e66-132">AzureRM.Websites</span></span>
* <span data-ttu-id="81e66-133">已修正未正確設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="81e66-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="81e66-134">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="81e66-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="81e66-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="81e66-135">AzureRM.Profile</span></span>
* <span data-ttu-id="81e66-136">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="81e66-137">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="81e66-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="81e66-138">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="81e66-139">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="81e66-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="81e66-140">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="81e66-140">Azure.Storage</span></span>
* <span data-ttu-id="81e66-141">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="81e66-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="81e66-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="81e66-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="81e66-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="81e66-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="81e66-144">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="81e66-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="81e66-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="81e66-146">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="81e66-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="81e66-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="81e66-148">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="81e66-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="81e66-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="81e66-150">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="81e66-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="81e66-151">AzureRM.Automation</span></span>
* <span data-ttu-id="81e66-152">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="81e66-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="81e66-153">AzureRM.Backup</span></span>
* <span data-ttu-id="81e66-154">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="81e66-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="81e66-155">AzureRM.Batch</span></span>
* <span data-ttu-id="81e66-156">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="81e66-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="81e66-157">AzureRM.Billing</span></span>
* <span data-ttu-id="81e66-158">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="81e66-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="81e66-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="81e66-160">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="81e66-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="81e66-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="81e66-162">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="81e66-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="81e66-163">AzureRM.Compute</span></span>
* <span data-ttu-id="81e66-164">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="81e66-165">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="81e66-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="81e66-166">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="81e66-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="81e66-167">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="81e66-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="81e66-168">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="81e66-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="81e66-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="81e66-170">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="81e66-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="81e66-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="81e66-172">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="81e66-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="81e66-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="81e66-174">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="81e66-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="81e66-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="81e66-176">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="81e66-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="81e66-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="81e66-178">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="81e66-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="81e66-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="81e66-180">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="81e66-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="81e66-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="81e66-182">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="81e66-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="81e66-183">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="81e66-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="81e66-184">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="81e66-185">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="81e66-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="81e66-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="81e66-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="81e66-187">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="81e66-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="81e66-188">AzureRM.Dns</span></span>
* <span data-ttu-id="81e66-189">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="81e66-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="81e66-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="81e66-191">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="81e66-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="81e66-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="81e66-193">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="81e66-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="81e66-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="81e66-195">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="81e66-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="81e66-196">AzureRM.Insights</span></span>
* <span data-ttu-id="81e66-197">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="81e66-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="81e66-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="81e66-199">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="81e66-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="81e66-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="81e66-201">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="81e66-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="81e66-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="81e66-203">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="81e66-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="81e66-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="81e66-205">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="81e66-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="81e66-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="81e66-207">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="81e66-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="81e66-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="81e66-209">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="81e66-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="81e66-210">AzureRM.Media</span></span>
* <span data-ttu-id="81e66-211">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="81e66-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="81e66-212">AzureRM.Network</span></span>
* <span data-ttu-id="81e66-213">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="81e66-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="81e66-214">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="81e66-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="81e66-215">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="81e66-216">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="81e66-217">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="81e66-218">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="81e66-219">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="81e66-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="81e66-220">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="81e66-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="81e66-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="81e66-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="81e66-222">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="81e66-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="81e66-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="81e66-224">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="81e66-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="81e66-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="81e66-226">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="81e66-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="81e66-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="81e66-228">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="81e66-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="81e66-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="81e66-230">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="81e66-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="81e66-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="81e66-232">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="81e66-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="81e66-233">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="81e66-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="81e66-234">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="81e66-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="81e66-235">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="81e66-236">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="81e66-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="81e66-237">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="81e66-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="81e66-238">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="81e66-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="81e66-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="81e66-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="81e66-240">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="81e66-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="81e66-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="81e66-242">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="81e66-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="81e66-243">AzureRM.Relay</span></span>
* <span data-ttu-id="81e66-244">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="81e66-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="81e66-245">AzureRM.Resources</span></span>
* <span data-ttu-id="81e66-246">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="81e66-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="81e66-247">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="81e66-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="81e66-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="81e66-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="81e66-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="81e66-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="81e66-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="81e66-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="81e66-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="81e66-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="81e66-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="81e66-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="81e66-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="81e66-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="81e66-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="81e66-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="81e66-255">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="81e66-256">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="81e66-257">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="81e66-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="81e66-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="81e66-259">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="81e66-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="81e66-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="81e66-261">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="81e66-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="81e66-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="81e66-263">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="81e66-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="81e66-264">AzureRM.Sql</span></span>
* <span data-ttu-id="81e66-265">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="81e66-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="81e66-266">AzureRM.Storage</span></span>
* <span data-ttu-id="81e66-267">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="81e66-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="81e66-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="81e66-269">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="81e66-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="81e66-270">AzureRM.Tags</span></span>
* <span data-ttu-id="81e66-271">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="81e66-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="81e66-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="81e66-273">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="81e66-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="81e66-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="81e66-275">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="81e66-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="81e66-276">AzureRM.Websites</span></span>
* <span data-ttu-id="81e66-277">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="81e66-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="81e66-278">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="81e66-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="81e66-279">一般</span><span class="sxs-lookup"><span data-stu-id="81e66-279">General</span></span>
* <span data-ttu-id="81e66-280">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="81e66-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="81e66-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="81e66-281">AzureRM.Profile</span></span>
* <span data-ttu-id="81e66-282">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="81e66-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="81e66-283">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="81e66-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="81e66-284">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="81e66-284">Azure.Storage</span></span>
* <span data-ttu-id="81e66-285">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="81e66-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="81e66-286">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="81e66-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="81e66-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="81e66-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="81e66-288">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="81e66-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="81e66-289">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="81e66-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="81e66-290">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="81e66-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="81e66-291">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="81e66-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="81e66-292">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="81e66-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="81e66-293">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="81e66-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="81e66-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="81e66-294">AzureRM.Compute</span></span>
* <span data-ttu-id="81e66-295">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="81e66-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="81e66-296">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="81e66-297">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="81e66-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="81e66-298">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="81e66-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="81e66-299">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="81e66-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="81e66-300">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="81e66-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="81e66-301">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="81e66-302">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="81e66-303">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="81e66-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="81e66-304">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="81e66-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="81e66-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="81e66-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="81e66-306">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="81e66-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="81e66-307">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="81e66-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="81e66-308">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81e66-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="81e66-309">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81e66-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="81e66-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="81e66-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="81e66-311">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="81e66-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="81e66-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="81e66-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="81e66-313">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="81e66-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="81e66-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="81e66-314">AzureRM.Insights</span></span>
* <span data-ttu-id="81e66-315">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="81e66-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="81e66-316">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="81e66-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="81e66-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="81e66-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="81e66-318">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="81e66-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="81e66-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="81e66-319">AzureRM.Network</span></span>
* <span data-ttu-id="81e66-320">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="81e66-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="81e66-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="81e66-321">AzureRM.Resources</span></span>
* <span data-ttu-id="81e66-322">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="81e66-323">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="81e66-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="81e66-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="81e66-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="81e66-325">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="81e66-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="81e66-326">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="81e66-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="81e66-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="81e66-327">AzureRM.Sql</span></span>
* <span data-ttu-id="81e66-328">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="81e66-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="81e66-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="81e66-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="81e66-330">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="81e66-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="81e66-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="81e66-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="81e66-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="81e66-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="81e66-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="81e66-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="81e66-334">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="81e66-335">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="81e66-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="81e66-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="81e66-336">AzureRM.Storage</span></span>
* <span data-ttu-id="81e66-337">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="81e66-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="81e66-338">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="81e66-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="81e66-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81e66-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="81e66-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81e66-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="81e66-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81e66-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="81e66-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="81e66-342">AzureRM.Tags</span></span>
* <span data-ttu-id="81e66-343">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="81e66-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="81e66-344">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="81e66-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="81e66-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="81e66-345">AzureRM.Profile</span></span>
* <span data-ttu-id="81e66-346">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="81e66-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="81e66-347">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="81e66-347">Azure.Storage</span></span>
* <span data-ttu-id="81e66-348">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="81e66-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="81e66-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="81e66-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="81e66-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="81e66-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="81e66-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="81e66-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="81e66-352">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="81e66-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="81e66-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="81e66-353">AzureRM.Automation</span></span>
* <span data-ttu-id="81e66-354">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="81e66-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="81e66-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="81e66-355">AzureRM.Compute</span></span>
* <span data-ttu-id="81e66-356">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="81e66-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="81e66-357">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="81e66-358">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="81e66-359">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="81e66-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="81e66-360">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="81e66-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="81e66-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="81e66-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="81e66-362">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="81e66-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="81e66-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="81e66-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="81e66-364">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="81e66-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="81e66-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="81e66-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="81e66-366">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="81e66-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="81e66-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="81e66-367">AzureRM.Network</span></span>
* <span data-ttu-id="81e66-368">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="81e66-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="81e66-369">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="81e66-370">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="81e66-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="81e66-371">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="81e66-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="81e66-372">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="81e66-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="81e66-373">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="81e66-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="81e66-374">AzureRM.Relay</span></span>
* <span data-ttu-id="81e66-375">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="81e66-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="81e66-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="81e66-376">AzureRM.Resources</span></span>
* <span data-ttu-id="81e66-377">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="81e66-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="81e66-378">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="81e66-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="81e66-379">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="81e66-380">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="81e66-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="81e66-381">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="81e66-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="81e66-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="81e66-383">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="81e66-384">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="81e66-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="81e66-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="81e66-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="81e66-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="81e66-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="81e66-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="81e66-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="81e66-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="81e66-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="81e66-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="81e66-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="81e66-390">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="81e66-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="81e66-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="81e66-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="81e66-392">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="81e66-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="81e66-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="81e66-393">AzureRM.Sql</span></span>
* <span data-ttu-id="81e66-394">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="81e66-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="81e66-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="81e66-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="81e66-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="81e66-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="81e66-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="81e66-397">AzureRM.Websites</span></span>
* <span data-ttu-id="81e66-398">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="81e66-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="81e66-399">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="81e66-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="81e66-400">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="81e66-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="81e66-401">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="81e66-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="81e66-402">一般</span><span class="sxs-lookup"><span data-stu-id="81e66-402">General</span></span>
* <span data-ttu-id="81e66-403">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="81e66-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="81e66-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="81e66-404">AzureRM.Profile</span></span>
* <span data-ttu-id="81e66-405">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="81e66-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="81e66-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="81e66-406">AzureRM.Compute</span></span>
* <span data-ttu-id="81e66-407">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="81e66-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="81e66-408">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="81e66-409">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="81e66-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="81e66-410">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="81e66-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="81e66-411">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81e66-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="81e66-412">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="81e66-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="81e66-413">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81e66-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="81e66-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="81e66-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="81e66-415">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="81e66-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="81e66-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="81e66-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="81e66-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="81e66-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="81e66-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="81e66-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="81e66-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="81e66-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="81e66-420">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="81e66-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="81e66-421">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="81e66-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="81e66-422">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="81e66-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="81e66-423">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="81e66-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="81e66-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="81e66-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="81e66-425">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="81e66-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="81e66-426">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="81e66-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="81e66-427">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="81e66-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="81e66-428">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="81e66-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="81e66-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="81e66-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="81e66-430">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="81e66-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="81e66-431">AzureRM.Network</span></span>
* <span data-ttu-id="81e66-432">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="81e66-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="81e66-433">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="81e66-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="81e66-434">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="81e66-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="81e66-435">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="81e66-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="81e66-436">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="81e66-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="81e66-437">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="81e66-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="81e66-438">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="81e66-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="81e66-439">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="81e66-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="81e66-440">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="81e66-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="81e66-441">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="81e66-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="81e66-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="81e66-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="81e66-443">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81e66-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="81e66-444">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="81e66-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="81e66-445">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="81e66-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="81e66-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="81e66-446">AzureRM.Resources</span></span>
* <span data-ttu-id="81e66-447">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="81e66-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="81e66-448">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="81e66-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="81e66-449">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="81e66-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="81e66-450">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="81e66-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="81e66-451">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="81e66-452">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="81e66-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="81e66-453">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="81e66-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="81e66-454">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="81e66-455">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="81e66-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="81e66-456">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="81e66-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="81e66-457">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="81e66-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="81e66-458">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="81e66-459">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="81e66-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="81e66-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="81e66-461">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="81e66-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="81e66-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="81e66-462">AzureRM.Sql</span></span>
* <span data-ttu-id="81e66-463">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="81e66-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="81e66-464">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="81e66-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="81e66-465">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="81e66-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="81e66-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="81e66-466">AzureRM.Profile</span></span>
* <span data-ttu-id="81e66-467">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="81e66-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="81e66-468">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="81e66-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="81e66-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="81e66-469">Azure.Storage</span></span>
* <span data-ttu-id="81e66-470">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="81e66-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="81e66-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="81e66-471">AzureRM.Compute</span></span>
* <span data-ttu-id="81e66-472">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="81e66-473">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="81e66-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="81e66-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="81e66-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="81e66-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="81e66-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="81e66-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="81e66-477">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="81e66-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="81e66-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="81e66-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="81e66-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="81e66-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="81e66-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="81e66-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="81e66-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="81e66-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="81e66-482">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="81e66-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="81e66-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81e66-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="81e66-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="81e66-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="81e66-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="81e66-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="81e66-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81e66-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="81e66-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81e66-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="81e66-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81e66-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="81e66-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="81e66-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="81e66-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="81e66-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="81e66-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="81e66-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="81e66-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="81e66-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="81e66-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="81e66-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="81e66-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="81e66-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="81e66-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="81e66-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="81e66-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="81e66-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="81e66-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="81e66-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="81e66-498">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="81e66-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="81e66-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="81e66-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="81e66-500">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="81e66-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="81e66-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="81e66-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="81e66-502">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="81e66-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="81e66-503">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="81e66-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="81e66-504">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="81e66-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="81e66-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="81e66-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="81e66-506">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81e66-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="81e66-507">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81e66-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="81e66-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="81e66-508">AzureRM.Sql</span></span>
* <span data-ttu-id="81e66-509">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="81e66-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="81e66-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="81e66-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="81e66-511">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="81e66-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="81e66-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="81e66-512">AzureRM.Websites</span></span>
* <span data-ttu-id="81e66-513">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="81e66-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="81e66-514">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="81e66-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="81e66-515">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="81e66-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="81e66-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="81e66-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="81e66-517">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="81e66-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="81e66-518">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="81e66-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="81e66-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="81e66-519">AzureRM.Profile</span></span>
* <span data-ttu-id="81e66-520">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="81e66-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="81e66-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="81e66-521">AzureRM.Compute</span></span>
* <span data-ttu-id="81e66-522">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="81e66-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="81e66-523">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="81e66-524">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="81e66-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="81e66-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="81e66-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="81e66-526">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="81e66-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="81e66-527">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="81e66-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="81e66-528">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="81e66-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="81e66-529">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="81e66-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="81e66-530">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="81e66-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="81e66-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="81e66-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="81e66-532">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="81e66-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="81e66-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="81e66-533">AzureRM.Network</span></span>
* <span data-ttu-id="81e66-534">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="81e66-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="81e66-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="81e66-535">AzureRM.Resources</span></span>
* <span data-ttu-id="81e66-536">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="81e66-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="81e66-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="81e66-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="81e66-538">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="81e66-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="81e66-539">AzureRM.Sql</span></span>
* <span data-ttu-id="81e66-540">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e66-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="81e66-541">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81e66-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="81e66-542">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="81e66-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="81e66-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="81e66-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="81e66-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="81e66-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="81e66-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81e66-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="81e66-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="81e66-546">AzureRM.Websites</span></span>
* <span data-ttu-id="81e66-547">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="81e66-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="81e66-548">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="81e66-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="81e66-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="81e66-549">AzureRM.Profile</span></span>
* <span data-ttu-id="81e66-550">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="81e66-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="81e66-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="81e66-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="81e66-552">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="81e66-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="81e66-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="81e66-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="81e66-554">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="81e66-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="81e66-555">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="81e66-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="81e66-556">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="81e66-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="81e66-557">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="81e66-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="81e66-558">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="81e66-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="81e66-559">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="81e66-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="81e66-560">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="81e66-560">Added support for MSI identity</span></span>
* <span data-ttu-id="81e66-561">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="81e66-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="81e66-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="81e66-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="81e66-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="81e66-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="81e66-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="81e66-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="81e66-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="81e66-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="81e66-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="81e66-566">AzureRM.Batch</span></span>
* <span data-ttu-id="81e66-567">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="81e66-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="81e66-568">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="81e66-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="81e66-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="81e66-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="81e66-570">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="81e66-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="81e66-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="81e66-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="81e66-572">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="81e66-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="81e66-573">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="81e66-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="81e66-574">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="81e66-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="81e66-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="81e66-575">AzureRM.Network</span></span>
* <span data-ttu-id="81e66-576">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="81e66-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="81e66-577">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="81e66-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="81e66-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="81e66-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="81e66-579">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="81e66-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="81e66-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="81e66-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="81e66-581">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="81e66-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="81e66-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="81e66-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="81e66-583">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="81e66-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="81e66-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="81e66-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="81e66-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="81e66-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="81e66-586">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="81e66-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="81e66-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="81e66-587">AzureRM.Sql</span></span>
* <span data-ttu-id="81e66-588">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="81e66-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="81e66-589">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="81e66-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="81e66-590">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="81e66-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="81e66-591">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="81e66-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="81e66-592">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="81e66-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="81e66-593">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81e66-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="81e66-594">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="81e66-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="81e66-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="81e66-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="81e66-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="81e66-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="81e66-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="81e66-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="81e66-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="81e66-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="81e66-599">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="81e66-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
