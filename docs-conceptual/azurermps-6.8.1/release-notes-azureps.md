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
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300828"
---
# <a name="release-notes"></a><span data-ttu-id="8e3a8-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="8e3a8-103">Release notes</span></span>

<span data-ttu-id="8e3a8-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="8e3a8-105">6.8.1 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8e3a8-106">一般</span><span class="sxs-lookup"><span data-stu-id="8e3a8-106">General</span></span>
* <span data-ttu-id="8e3a8-107">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="8e3a8-108">已更新通用執行階段組件</span><span class="sxs-lookup"><span data-stu-id="8e3a8-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8e3a8-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e3a8-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8e3a8-110">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="8e3a8-111">已修正的問題 https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="8e3a8-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="8e3a8-112">Import-AzureRmApiManagementApi 和 \*-AzureRmApiManagementCertificate cmdlets 目前處理相對路徑</span><span class="sxs-lookup"><span data-stu-id="8e3a8-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="8e3a8-113">已修正的問題 https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="8e3a8-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="8e3a8-114">CertificateInformation 為可設定的屬性，允許 Set-AzureRmApiManagement Cmdlet 正常運作。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="8e3a8-115">已藉由升級至 4.0.4-preview NuGet 而修正</span><span class="sxs-lookup"><span data-stu-id="8e3a8-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="8e3a8-116">已修正的問題 https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="8e3a8-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="8e3a8-117">已修正依產品名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="8e3a8-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="8e3a8-118">已修正的問題 https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="8e3a8-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="8e3a8-119">已修正依 API 名稱搜尋的 Odata 篩選條件</span><span class="sxs-lookup"><span data-stu-id="8e3a8-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="8e3a8-120">已新增對 AzureMonitor 記錄器的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="8e3a8-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-121">AzureRM.Compute</span></span>
* <span data-ttu-id="8e3a8-122">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="8e3a8-123">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="8e3a8-124">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="8e3a8-125">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="8e3a8-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8e3a8-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8e3a8-126">AzureRM.Network</span></span>
* <span data-ttu-id="8e3a8-127">已將預設的 Cmdlet 輸出表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="8e3a8-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8e3a8-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8e3a8-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8e3a8-129">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="8e3a8-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="8e3a8-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8e3a8-130">AzureRM.Resources</span></span>
* <span data-ttu-id="8e3a8-131">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8e3a8-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e3a8-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8e3a8-133">已修正的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8e3a8-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8e3a8-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8e3a8-135">已新增對 MultiValue 路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="8e3a8-136">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="8e3a8-137">已新增對子網路路由方法的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="8e3a8-138">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="8e3a8-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="8e3a8-139">已新增對設定檔中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="8e3a8-140">已新增對設定檔中預期狀態碼的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="8e3a8-141">已新增對端點中自訂標頭的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="8e3a8-142">6.8.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8e3a8-143">一般</span><span class="sxs-lookup"><span data-stu-id="8e3a8-143">General</span></span>
* <span data-ttu-id="8e3a8-144">已修正未設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8e3a8-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-145">AzureRM.Profile</span></span>
* <span data-ttu-id="8e3a8-146">已將到期屬性新增至在 Connect-AzureRmAccount 期間傳回的權杖</span><span class="sxs-lookup"><span data-stu-id="8e3a8-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8e3a8-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-147">AzureRM.Compute</span></span>
* <span data-ttu-id="8e3a8-148">已修正在錯誤輸出中遺漏目標的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="8e3a8-149">已修正搭配受控磁碟的 VM 之儲存體帳戶類型的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="8e3a8-150">修正適用於其他環境的 AEM 擴充 Cmdlet，例如 Azure China</span><span class="sxs-lookup"><span data-stu-id="8e3a8-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="8e3a8-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e3a8-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="8e3a8-152">修正 New-AzureRmIotHubExportDevices 和 New-AzureRmIotHubImportDevices 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8e3a8-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8e3a8-153">AzureRM.Network</span></span>
* <span data-ttu-id="8e3a8-154">已將預設模式表示法變更為資料表檢視</span><span class="sxs-lookup"><span data-stu-id="8e3a8-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8e3a8-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8e3a8-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8e3a8-156">修正在嘗試調整已暫停的容量時，Update-AzureRmPowerBIEmbeddedCapacity 中發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="8e3a8-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8e3a8-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8e3a8-157">AzureRM.Resources</span></span>
* <span data-ttu-id="8e3a8-158">已修正從 MarketPlace 建立受控應用程式發生的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8e3a8-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e3a8-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8e3a8-160">修正問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8e3a8-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8e3a8-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8e3a8-162">支援 MultiValue 路由方法</span><span class="sxs-lookup"><span data-stu-id="8e3a8-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="8e3a8-163">為 MultiValue 路由新增 'MaxReturn' 參數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="8e3a8-164">支援子網路路由方法</span><span class="sxs-lookup"><span data-stu-id="8e3a8-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="8e3a8-165">支援端點中的 IP 位址範圍 (子網路)</span><span class="sxs-lookup"><span data-stu-id="8e3a8-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="8e3a8-166">支援設定檔中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="8e3a8-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="8e3a8-167">支援設定檔中的預期狀態碼</span><span class="sxs-lookup"><span data-stu-id="8e3a8-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="8e3a8-168">支援端點中的自訂標頭</span><span class="sxs-lookup"><span data-stu-id="8e3a8-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8e3a8-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8e3a8-169">AzureRM.Websites</span></span>
* <span data-ttu-id="8e3a8-170">已修正未正確設定預設資源群組的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="8e3a8-171">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8e3a8-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-172">AzureRM.Profile</span></span>
* <span data-ttu-id="8e3a8-173">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8e3a8-174">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="8e3a8-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="8e3a8-175">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="8e3a8-176">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="8e3a8-177">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-177">Azure.Storage</span></span>
* <span data-ttu-id="8e3a8-178">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="8e3a8-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="8e3a8-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8e3a8-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8e3a8-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8e3a8-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8e3a8-181">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="8e3a8-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8e3a8-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="8e3a8-183">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8e3a8-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e3a8-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8e3a8-185">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="8e3a8-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8e3a8-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="8e3a8-187">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8e3a8-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8e3a8-188">AzureRM.Automation</span></span>
* <span data-ttu-id="8e3a8-189">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="8e3a8-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="8e3a8-190">AzureRM.Backup</span></span>
* <span data-ttu-id="8e3a8-191">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8e3a8-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8e3a8-192">AzureRM.Batch</span></span>
* <span data-ttu-id="8e3a8-193">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="8e3a8-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="8e3a8-194">AzureRM.Billing</span></span>
* <span data-ttu-id="8e3a8-195">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="8e3a8-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="8e3a8-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="8e3a8-197">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="8e3a8-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8e3a8-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="8e3a8-199">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8e3a8-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-200">AzureRM.Compute</span></span>
* <span data-ttu-id="8e3a8-201">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8e3a8-202">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8e3a8-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="8e3a8-203">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="8e3a8-204">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="8e3a8-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8e3a8-205">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8e3a8-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8e3a8-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="8e3a8-207">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="8e3a8-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8e3a8-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="8e3a8-209">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="8e3a8-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8e3a8-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="8e3a8-211">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="8e3a8-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="8e3a8-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="8e3a8-213">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8e3a8-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8e3a8-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8e3a8-215">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8e3a8-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8e3a8-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8e3a8-217">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8e3a8-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e3a8-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8e3a8-219">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="8e3a8-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="8e3a8-220">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8e3a8-221">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8e3a8-222">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="8e3a8-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="8e3a8-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="8e3a8-224">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="8e3a8-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="8e3a8-225">AzureRM.Dns</span></span>
* <span data-ttu-id="8e3a8-226">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8e3a8-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8e3a8-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8e3a8-228">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8e3a8-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e3a8-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="8e3a8-230">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="8e3a8-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8e3a8-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="8e3a8-232">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8e3a8-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8e3a8-233">AzureRM.Insights</span></span>
* <span data-ttu-id="8e3a8-234">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="8e3a8-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="8e3a8-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="8e3a8-236">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8e3a8-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e3a8-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8e3a8-238">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8e3a8-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8e3a8-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8e3a8-240">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="8e3a8-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8e3a8-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="8e3a8-242">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="8e3a8-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="8e3a8-244">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="8e3a8-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8e3a8-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="8e3a8-246">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="8e3a8-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="8e3a8-247">AzureRM.Media</span></span>
* <span data-ttu-id="8e3a8-248">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8e3a8-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8e3a8-249">AzureRM.Network</span></span>
* <span data-ttu-id="8e3a8-250">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="8e3a8-251">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="8e3a8-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8e3a8-252">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="8e3a8-253">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="8e3a8-254">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="8e3a8-255">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8e3a8-256">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="8e3a8-257">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="8e3a8-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="8e3a8-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8e3a8-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="8e3a8-259">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="8e3a8-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e3a8-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8e3a8-261">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8e3a8-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8e3a8-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8e3a8-263">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8e3a8-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8e3a8-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8e3a8-265">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="8e3a8-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8e3a8-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="8e3a8-267">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8e3a8-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8e3a8-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8e3a8-269">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="8e3a8-270">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="8e3a8-271">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="8e3a8-272">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8e3a8-273">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="8e3a8-274">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="8e3a8-275">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="8e3a8-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8e3a8-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8e3a8-277">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="8e3a8-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8e3a8-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="8e3a8-279">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8e3a8-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8e3a8-280">AzureRM.Relay</span></span>
* <span data-ttu-id="8e3a8-281">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8e3a8-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8e3a8-282">AzureRM.Resources</span></span>
* <span data-ttu-id="8e3a8-283">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="8e3a8-284">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="8e3a8-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8e3a8-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="8e3a8-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8e3a8-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="8e3a8-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8e3a8-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="8e3a8-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8e3a8-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="8e3a8-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8e3a8-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="8e3a8-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8e3a8-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="8e3a8-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8e3a8-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="8e3a8-292">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="8e3a8-293">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="8e3a8-294">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8e3a8-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8e3a8-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8e3a8-296">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8e3a8-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e3a8-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8e3a8-298">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8e3a8-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e3a8-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8e3a8-300">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8e3a8-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8e3a8-301">AzureRM.Sql</span></span>
* <span data-ttu-id="8e3a8-302">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8e3a8-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-303">AzureRM.Storage</span></span>
* <span data-ttu-id="8e3a8-304">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="8e3a8-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="8e3a8-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="8e3a8-306">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="8e3a8-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="8e3a8-307">AzureRM.Tags</span></span>
* <span data-ttu-id="8e3a8-308">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8e3a8-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8e3a8-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8e3a8-310">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="8e3a8-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="8e3a8-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="8e3a8-312">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8e3a8-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8e3a8-313">AzureRM.Websites</span></span>
* <span data-ttu-id="8e3a8-314">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="8e3a8-315">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8e3a8-316">一般</span><span class="sxs-lookup"><span data-stu-id="8e3a8-316">General</span></span>
* <span data-ttu-id="8e3a8-317">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8e3a8-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-318">AzureRM.Profile</span></span>
* <span data-ttu-id="8e3a8-319">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="8e3a8-320">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8e3a8-321">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-321">Azure.Storage</span></span>
* <span data-ttu-id="8e3a8-322">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="8e3a8-323">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8e3a8-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e3a8-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8e3a8-325">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="8e3a8-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="8e3a8-326">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="8e3a8-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="8e3a8-327">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="8e3a8-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="8e3a8-328">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="8e3a8-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="8e3a8-329">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="8e3a8-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="8e3a8-330">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="8e3a8-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8e3a8-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-331">AzureRM.Compute</span></span>
* <span data-ttu-id="8e3a8-332">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="8e3a8-333">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="8e3a8-334">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="8e3a8-335">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="8e3a8-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="8e3a8-336">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="8e3a8-337">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="8e3a8-338">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="8e3a8-339">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="8e3a8-340">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="8e3a8-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="8e3a8-341">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8e3a8-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8e3a8-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8e3a8-343">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="8e3a8-344">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="8e3a8-345">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="8e3a8-346">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8e3a8-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e3a8-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8e3a8-348">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="8e3a8-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8e3a8-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e3a8-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="8e3a8-350">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="8e3a8-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8e3a8-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8e3a8-351">AzureRM.Insights</span></span>
* <span data-ttu-id="8e3a8-352">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="8e3a8-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="8e3a8-353">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="8e3a8-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8e3a8-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e3a8-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8e3a8-355">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8e3a8-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8e3a8-356">AzureRM.Network</span></span>
* <span data-ttu-id="8e3a8-357">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8e3a8-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8e3a8-358">AzureRM.Resources</span></span>
* <span data-ttu-id="8e3a8-359">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="8e3a8-360">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="8e3a8-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8e3a8-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e3a8-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8e3a8-362">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="8e3a8-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="8e3a8-363">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="8e3a8-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8e3a8-364">AzureRM.Sql</span></span>
* <span data-ttu-id="8e3a8-365">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="8e3a8-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8e3a8-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8e3a8-367">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="8e3a8-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="8e3a8-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="8e3a8-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="8e3a8-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="8e3a8-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="8e3a8-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="8e3a8-371">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="8e3a8-372">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="8e3a8-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8e3a8-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-373">AzureRM.Storage</span></span>
* <span data-ttu-id="8e3a8-374">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="8e3a8-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="8e3a8-375">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="8e3a8-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="8e3a8-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e3a8-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="8e3a8-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e3a8-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="8e3a8-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8e3a8-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="8e3a8-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="8e3a8-379">AzureRM.Tags</span></span>
* <span data-ttu-id="8e3a8-380">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="8e3a8-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="8e3a8-381">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8e3a8-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-382">AzureRM.Profile</span></span>
* <span data-ttu-id="8e3a8-383">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="8e3a8-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8e3a8-384">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-384">Azure.Storage</span></span>
* <span data-ttu-id="8e3a8-385">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="8e3a8-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="8e3a8-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8e3a8-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="8e3a8-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8e3a8-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8e3a8-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8e3a8-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8e3a8-389">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8e3a8-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8e3a8-390">AzureRM.Automation</span></span>
* <span data-ttu-id="8e3a8-391">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8e3a8-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-392">AzureRM.Compute</span></span>
* <span data-ttu-id="8e3a8-393">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="8e3a8-394">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8e3a8-395">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8e3a8-396">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="8e3a8-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="8e3a8-397">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8e3a8-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e3a8-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="8e3a8-399">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8e3a8-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e3a8-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8e3a8-401">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8e3a8-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8e3a8-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8e3a8-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8e3a8-403">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="8e3a8-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8e3a8-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8e3a8-404">AzureRM.Network</span></span>
* <span data-ttu-id="8e3a8-405">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="8e3a8-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="8e3a8-406">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="8e3a8-407">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="8e3a8-408">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="8e3a8-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="8e3a8-409">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="8e3a8-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="8e3a8-410">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8e3a8-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8e3a8-411">AzureRM.Relay</span></span>
* <span data-ttu-id="8e3a8-412">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8e3a8-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8e3a8-413">AzureRM.Resources</span></span>
* <span data-ttu-id="8e3a8-414">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="8e3a8-415">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="8e3a8-416">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="8e3a8-417">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="8e3a8-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="8e3a8-418">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8e3a8-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e3a8-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8e3a8-420">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="8e3a8-421">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="8e3a8-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8e3a8-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8e3a8-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8e3a8-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8e3a8-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8e3a8-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8e3a8-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8e3a8-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8e3a8-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8e3a8-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="8e3a8-427">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8e3a8-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e3a8-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8e3a8-429">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8e3a8-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8e3a8-430">AzureRM.Sql</span></span>
* <span data-ttu-id="8e3a8-431">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="8e3a8-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="8e3a8-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8e3a8-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="8e3a8-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8e3a8-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8e3a8-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8e3a8-434">AzureRM.Websites</span></span>
* <span data-ttu-id="8e3a8-435">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="8e3a8-436">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="8e3a8-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="8e3a8-437">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="8e3a8-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="8e3a8-438">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8e3a8-439">一般</span><span class="sxs-lookup"><span data-stu-id="8e3a8-439">General</span></span>
* <span data-ttu-id="8e3a8-440">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="8e3a8-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8e3a8-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-441">AzureRM.Profile</span></span>
* <span data-ttu-id="8e3a8-442">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="8e3a8-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8e3a8-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-443">AzureRM.Compute</span></span>
* <span data-ttu-id="8e3a8-444">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="8e3a8-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="8e3a8-445">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="8e3a8-446">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8e3a8-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="8e3a8-447">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="8e3a8-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="8e3a8-448">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8e3a8-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="8e3a8-449">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="8e3a8-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="8e3a8-450">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8e3a8-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8e3a8-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8e3a8-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8e3a8-452">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="8e3a8-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8e3a8-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8e3a8-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8e3a8-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8e3a8-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8e3a8-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8e3a8-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e3a8-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8e3a8-457">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="8e3a8-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8e3a8-458">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8e3a8-459">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="8e3a8-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="8e3a8-460">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="8e3a8-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8e3a8-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8e3a8-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="8e3a8-462">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8e3a8-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="8e3a8-463">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="8e3a8-464">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="8e3a8-465">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8e3a8-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e3a8-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8e3a8-467">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8e3a8-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8e3a8-468">AzureRM.Network</span></span>
* <span data-ttu-id="8e3a8-469">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="8e3a8-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="8e3a8-470">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="8e3a8-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="8e3a8-471">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8e3a8-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8e3a8-472">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8e3a8-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8e3a8-473">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8e3a8-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8e3a8-474">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8e3a8-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8e3a8-475">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8e3a8-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8e3a8-476">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8e3a8-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8e3a8-477">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8e3a8-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8e3a8-478">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8e3a8-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8e3a8-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8e3a8-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8e3a8-480">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="8e3a8-481">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="8e3a8-482">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8e3a8-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8e3a8-483">AzureRM.Resources</span></span>
* <span data-ttu-id="8e3a8-484">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="8e3a8-485">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="8e3a8-486">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="8e3a8-487">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="8e3a8-488">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="8e3a8-489">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="8e3a8-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8e3a8-490">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="8e3a8-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8e3a8-491">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="8e3a8-492">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="8e3a8-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8e3a8-493">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="8e3a8-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8e3a8-494">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="8e3a8-495">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="8e3a8-496">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="8e3a8-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8e3a8-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8e3a8-498">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8e3a8-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8e3a8-499">AzureRM.Sql</span></span>
* <span data-ttu-id="8e3a8-500">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="8e3a8-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="8e3a8-501">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="8e3a8-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="8e3a8-502">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8e3a8-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-503">AzureRM.Profile</span></span>
* <span data-ttu-id="8e3a8-504">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="8e3a8-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="8e3a8-505">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="8e3a8-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8e3a8-506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-506">Azure.Storage</span></span>
* <span data-ttu-id="8e3a8-507">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8e3a8-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-508">AzureRM.Compute</span></span>
* <span data-ttu-id="8e3a8-509">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="8e3a8-510">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="8e3a8-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8e3a8-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8e3a8-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8e3a8-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8e3a8-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8e3a8-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8e3a8-514">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="8e3a8-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8e3a8-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="8e3a8-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8e3a8-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="8e3a8-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8e3a8-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="8e3a8-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8e3a8-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="8e3a8-519">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="8e3a8-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="8e3a8-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8e3a8-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="8e3a8-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="8e3a8-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="8e3a8-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="8e3a8-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="8e3a8-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8e3a8-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="8e3a8-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8e3a8-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="8e3a8-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8e3a8-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="8e3a8-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8e3a8-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="8e3a8-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8e3a8-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="8e3a8-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8e3a8-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8e3a8-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="8e3a8-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="8e3a8-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8e3a8-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8e3a8-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="8e3a8-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="8e3a8-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8e3a8-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="8e3a8-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8e3a8-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8e3a8-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8e3a8-535">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8e3a8-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e3a8-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8e3a8-537">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="8e3a8-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8e3a8-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8e3a8-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8e3a8-539">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="8e3a8-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="8e3a8-540">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="8e3a8-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="8e3a8-541">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="8e3a8-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8e3a8-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8e3a8-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8e3a8-543">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="8e3a8-544">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8e3a8-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8e3a8-545">AzureRM.Sql</span></span>
* <span data-ttu-id="8e3a8-546">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8e3a8-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8e3a8-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8e3a8-548">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8e3a8-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8e3a8-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8e3a8-549">AzureRM.Websites</span></span>
* <span data-ttu-id="8e3a8-550">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="8e3a8-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="8e3a8-551">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="8e3a8-552">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="8e3a8-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8e3a8-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8e3a8-554">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="8e3a8-555">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8e3a8-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-556">AzureRM.Profile</span></span>
* <span data-ttu-id="8e3a8-557">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="8e3a8-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8e3a8-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8e3a8-558">AzureRM.Compute</span></span>
* <span data-ttu-id="8e3a8-559">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="8e3a8-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="8e3a8-560">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="8e3a8-561">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8e3a8-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8e3a8-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8e3a8-563">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="8e3a8-564">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="8e3a8-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="8e3a8-565">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="8e3a8-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="8e3a8-566">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="8e3a8-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="8e3a8-567">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="8e3a8-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="8e3a8-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8e3a8-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8e3a8-569">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="8e3a8-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="8e3a8-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8e3a8-570">AzureRM.Network</span></span>
* <span data-ttu-id="8e3a8-571">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="8e3a8-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8e3a8-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8e3a8-572">AzureRM.Resources</span></span>
* <span data-ttu-id="8e3a8-573">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8e3a8-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8e3a8-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8e3a8-575">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="8e3a8-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8e3a8-576">AzureRM.Sql</span></span>
* <span data-ttu-id="8e3a8-577">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e3a8-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="8e3a8-578">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e3a8-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8e3a8-579">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8e3a8-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8e3a8-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8e3a8-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8e3a8-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8e3a8-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8e3a8-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e3a8-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8e3a8-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8e3a8-583">AzureRM.Websites</span></span>
* <span data-ttu-id="8e3a8-584">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="8e3a8-585">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="8e3a8-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8e3a8-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8e3a8-586">AzureRM.Profile</span></span>
* <span data-ttu-id="8e3a8-587">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="8e3a8-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8e3a8-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8e3a8-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8e3a8-589">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8e3a8-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8e3a8-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8e3a8-591">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="8e3a8-592">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="8e3a8-593">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="8e3a8-594">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="8e3a8-595">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="8e3a8-596">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="8e3a8-597">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="8e3a8-597">Added support for MSI identity</span></span>
* <span data-ttu-id="8e3a8-598">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="8e3a8-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="8e3a8-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="8e3a8-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="8e3a8-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e3a8-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="8e3a8-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="8e3a8-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="8e3a8-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="8e3a8-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8e3a8-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8e3a8-603">AzureRM.Batch</span></span>
* <span data-ttu-id="8e3a8-604">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="8e3a8-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="8e3a8-605">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="8e3a8-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8e3a8-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8e3a8-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="8e3a8-607">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="8e3a8-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8e3a8-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8e3a8-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8e3a8-609">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="8e3a8-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8e3a8-610">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="8e3a8-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="8e3a8-611">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="8e3a8-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="8e3a8-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8e3a8-612">AzureRM.Network</span></span>
* <span data-ttu-id="8e3a8-613">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="8e3a8-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="8e3a8-614">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="8e3a8-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="8e3a8-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e3a8-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="8e3a8-616">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="8e3a8-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8e3a8-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8e3a8-618">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="8e3a8-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8e3a8-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8e3a8-620">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="8e3a8-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="8e3a8-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8e3a8-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8e3a8-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8e3a8-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8e3a8-623">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="8e3a8-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8e3a8-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8e3a8-624">AzureRM.Sql</span></span>
* <span data-ttu-id="8e3a8-625">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="8e3a8-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="8e3a8-626">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="8e3a8-627">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="8e3a8-628">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="8e3a8-629">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="8e3a8-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="8e3a8-630">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e3a8-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8e3a8-631">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8e3a8-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8e3a8-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8e3a8-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8e3a8-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8e3a8-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8e3a8-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e3a8-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8e3a8-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8e3a8-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8e3a8-636">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="8e3a8-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
