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
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018930"
---
# <a name="release-notes"></a><span data-ttu-id="9eb5f-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="9eb5f-103">Release notes</span></span>

<span data-ttu-id="9eb5f-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="9eb5f-105">6.7.0 - 2018 年 8 月</span><span class="sxs-lookup"><span data-stu-id="9eb5f-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9eb5f-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9eb5f-106">AzureRM.Profile</span></span>
* <span data-ttu-id="9eb5f-107">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="9eb5f-108">將使用者識別碼新增至預設內容名稱，以避免內容發生衝突</span><span class="sxs-lookup"><span data-stu-id="9eb5f-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="9eb5f-109">修正 Clear-AzureRmContext 在選擇內容 #6398 時出現的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="9eb5f-110">允許將租用戶網域傳遞給 'Connect-AzureRmAccount' 的 '-TenantId' 參數</span><span class="sxs-lookup"><span data-stu-id="9eb5f-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="9eb5f-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-111">Azure.Storage</span></span>
* <span data-ttu-id="9eb5f-112">移除 Azure 檔案共用 5TB 的配額限制</span><span class="sxs-lookup"><span data-stu-id="9eb5f-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="9eb5f-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="9eb5f-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="9eb5f-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9eb5f-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="9eb5f-115">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="9eb5f-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9eb5f-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="9eb5f-117">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="9eb5f-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9eb5f-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="9eb5f-119">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="9eb5f-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="9eb5f-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="9eb5f-121">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="9eb5f-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="9eb5f-122">AzureRM.Automation</span></span>
* <span data-ttu-id="9eb5f-123">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="9eb5f-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="9eb5f-124">AzureRM.Backup</span></span>
* <span data-ttu-id="9eb5f-125">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="9eb5f-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="9eb5f-126">AzureRM.Batch</span></span>
* <span data-ttu-id="9eb5f-127">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="9eb5f-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="9eb5f-128">AzureRM.Billing</span></span>
* <span data-ttu-id="9eb5f-129">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="9eb5f-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="9eb5f-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="9eb5f-131">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="9eb5f-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="9eb5f-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="9eb5f-133">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9eb5f-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9eb5f-134">AzureRM.Compute</span></span>
* <span data-ttu-id="9eb5f-135">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="9eb5f-136">將 EvictionPolicy 參數新增至 New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9eb5f-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="9eb5f-137">若未指定位置，則使用 New-AzureRmVm 的 DiskFileParameterSet 中的預設位置。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="9eb5f-138">修正 Save-AzureRmVMImage 中的參數描述</span><span class="sxs-lookup"><span data-stu-id="9eb5f-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="9eb5f-139">修正某些單次傳遞相關案例的 Get-AzureRmVMDiskEncryptionStatus Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="9eb5f-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="9eb5f-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="9eb5f-141">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="9eb5f-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="9eb5f-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="9eb5f-143">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="9eb5f-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9eb5f-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="9eb5f-145">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="9eb5f-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="9eb5f-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="9eb5f-147">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="9eb5f-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9eb5f-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="9eb5f-149">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="9eb5f-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9eb5f-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="9eb5f-151">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9eb5f-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9eb5f-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9eb5f-153">修正從 PowerShell 命令列設定 DebugPreference 時的偵錯問</span><span class="sxs-lookup"><span data-stu-id="9eb5f-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="9eb5f-154">更新 Set-AzureRmDataLakeStoreItemAcl 範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="9eb5f-155">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="9eb5f-156">更新 Set-AzureRmDataLakeStoreItemAclEntry 範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="9eb5f-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="9eb5f-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="9eb5f-158">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="9eb5f-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="9eb5f-159">AzureRM.Dns</span></span>
* <span data-ttu-id="9eb5f-160">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="9eb5f-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9eb5f-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="9eb5f-162">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="9eb5f-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="9eb5f-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="9eb5f-164">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="9eb5f-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="9eb5f-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="9eb5f-166">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="9eb5f-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="9eb5f-167">AzureRM.Insights</span></span>
* <span data-ttu-id="9eb5f-168">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="9eb5f-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="9eb5f-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="9eb5f-170">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9eb5f-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9eb5f-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9eb5f-172">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="9eb5f-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9eb5f-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="9eb5f-174">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="9eb5f-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9eb5f-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="9eb5f-176">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="9eb5f-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="9eb5f-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="9eb5f-178">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="9eb5f-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="9eb5f-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="9eb5f-180">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="9eb5f-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="9eb5f-181">AzureRM.Media</span></span>
* <span data-ttu-id="9eb5f-182">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9eb5f-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9eb5f-183">AzureRM.Network</span></span>
* <span data-ttu-id="9eb5f-184">已新增 Set-AzureRmLocalNetworkGateway 範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="9eb5f-185">已新增 Add-AzureRmVirtualNetworkGatewayIpConfig、Get-AzureRmVirtualNetworkGatewayConnectionSharedKey 和 New-AzureRmVirtualNetworkGatewayConnection 的範例和描述</span><span class="sxs-lookup"><span data-stu-id="9eb5f-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="9eb5f-186">已新增 Remove-AzureRmVirtualNetworkGatewayIpConfig 和 Reset-AzureRmVirtualNetworkGateway 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="9eb5f-187">已新增 Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="9eb5f-188">已新增 Set-AzureRmVirtualNetworkGatewayConnectionSharedKey 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="9eb5f-189">已新增 Set-AzureRmVirtualNetworkGatewayConnection 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="9eb5f-190">已使用最新的程式碼產生器重新產生 ApplicationSecurityGroup、RouteTable 和 Usage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="9eb5f-191">已釐清在嘗試取得未結束的子網路時，Get-AzureRmVirtualNetworkSubnetConfig 出現的錯誤</span><span class="sxs-lookup"><span data-stu-id="9eb5f-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="9eb5f-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="9eb5f-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="9eb5f-193">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="9eb5f-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9eb5f-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="9eb5f-195">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="9eb5f-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9eb5f-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="9eb5f-197">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="9eb5f-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="9eb5f-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="9eb5f-199">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="9eb5f-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9eb5f-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="9eb5f-201">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="9eb5f-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9eb5f-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9eb5f-203">已將原則篩選條件新增至 Get-AzureRmRecoveryServicesBackItem Xmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="9eb5f-204">命令會傳回受指定原則識別碼保護的備份項目清單。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="9eb5f-205">已將 Microsoft.Azure.Management.RecoveryServices.Backup 更新為版本 3.0.0-preview。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="9eb5f-206">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="9eb5f-207">已將 TargetResourceGroupName 參數新增至 Restore-AzureRmRecoveryServicesBackupItem。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="9eb5f-208">受控磁碟還原的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="9eb5f-209">適用於具有受控磁碟的 VM 備份。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="9eb5f-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9eb5f-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="9eb5f-211">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="9eb5f-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="9eb5f-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="9eb5f-213">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="9eb5f-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="9eb5f-214">AzureRM.Relay</span></span>
* <span data-ttu-id="9eb5f-215">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9eb5f-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9eb5f-216">AzureRM.Resources</span></span>
* <span data-ttu-id="9eb5f-217">支援在訂用帳戶範圍部署範本。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="9eb5f-218">新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="9eb5f-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9eb5f-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="9eb5f-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9eb5f-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="9eb5f-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9eb5f-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="9eb5f-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9eb5f-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="9eb5f-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="9eb5f-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="9eb5f-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="9eb5f-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="9eb5f-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="9eb5f-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="9eb5f-226">修正在將內容傳遞至 Set-AzureRmResource 時擲回錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="9eb5f-227">修正 New-AzureRmResourceGroupDeployment 中的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="9eb5f-228">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="9eb5f-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="9eb5f-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="9eb5f-230">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9eb5f-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9eb5f-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9eb5f-232">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="9eb5f-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9eb5f-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="9eb5f-234">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9eb5f-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9eb5f-235">AzureRM.Sql</span></span>
* <span data-ttu-id="9eb5f-236">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="9eb5f-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-237">AzureRM.Storage</span></span>
* <span data-ttu-id="9eb5f-238">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="9eb5f-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="9eb5f-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="9eb5f-240">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="9eb5f-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="9eb5f-241">AzureRM.Tags</span></span>
* <span data-ttu-id="9eb5f-242">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="9eb5f-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9eb5f-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="9eb5f-244">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="9eb5f-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="9eb5f-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="9eb5f-246">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9eb5f-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9eb5f-247">AzureRM.Websites</span></span>
* <span data-ttu-id="9eb5f-248">已更新至最新版本的 Azure ClientRuntime。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="9eb5f-249">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="9eb5f-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9eb5f-250">一般</span><span class="sxs-lookup"><span data-stu-id="9eb5f-250">General</span></span>
* <span data-ttu-id="9eb5f-251">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="9eb5f-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9eb5f-252">AzureRM.Profile</span></span>
* <span data-ttu-id="9eb5f-253">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="9eb5f-254">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="9eb5f-255">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-255">Azure.Storage</span></span>
* <span data-ttu-id="9eb5f-256">已新增從 DefaultProfile 取得儲存體內容的支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="9eb5f-257">已將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="9eb5f-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9eb5f-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="9eb5f-259">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="9eb5f-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="9eb5f-260">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="9eb5f-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="9eb5f-261">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="9eb5f-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="9eb5f-262">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="9eb5f-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="9eb5f-263">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="9eb5f-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="9eb5f-264">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="9eb5f-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9eb5f-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9eb5f-265">AzureRM.Compute</span></span>
* <span data-ttu-id="9eb5f-266">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="9eb5f-267">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="9eb5f-268">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="9eb5f-269">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="9eb5f-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="9eb5f-270">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="9eb5f-271">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="9eb5f-272">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="9eb5f-273">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="9eb5f-274">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="9eb5f-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="9eb5f-275">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="9eb5f-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9eb5f-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="9eb5f-277">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="9eb5f-278">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="9eb5f-279">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="9eb5f-280">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9eb5f-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9eb5f-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9eb5f-282">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="9eb5f-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="9eb5f-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="9eb5f-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="9eb5f-284">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="9eb5f-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="9eb5f-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="9eb5f-285">AzureRM.Insights</span></span>
* <span data-ttu-id="9eb5f-286">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="9eb5f-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="9eb5f-287">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="9eb5f-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9eb5f-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9eb5f-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9eb5f-289">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9eb5f-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9eb5f-290">AzureRM.Network</span></span>
* <span data-ttu-id="9eb5f-291">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9eb5f-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9eb5f-292">AzureRM.Resources</span></span>
* <span data-ttu-id="9eb5f-293">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="9eb5f-294">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="9eb5f-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9eb5f-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9eb5f-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9eb5f-296">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="9eb5f-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="9eb5f-297">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="9eb5f-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9eb5f-298">AzureRM.Sql</span></span>
* <span data-ttu-id="9eb5f-299">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="9eb5f-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9eb5f-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="9eb5f-301">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="9eb5f-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="9eb5f-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="9eb5f-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="9eb5f-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="9eb5f-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="9eb5f-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="9eb5f-305">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="9eb5f-306">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="9eb5f-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="9eb5f-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-307">AzureRM.Storage</span></span>
* <span data-ttu-id="9eb5f-308">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="9eb5f-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="9eb5f-309">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="9eb5f-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="9eb5f-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9eb5f-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="9eb5f-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9eb5f-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="9eb5f-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9eb5f-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="9eb5f-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="9eb5f-313">AzureRM.Tags</span></span>
* <span data-ttu-id="9eb5f-314">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="9eb5f-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="9eb5f-315">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="9eb5f-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9eb5f-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9eb5f-316">AzureRM.Profile</span></span>
* <span data-ttu-id="9eb5f-317">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="9eb5f-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="9eb5f-318">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-318">Azure.Storage</span></span>
* <span data-ttu-id="9eb5f-319">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="9eb5f-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="9eb5f-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9eb5f-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="9eb5f-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9eb5f-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="9eb5f-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9eb5f-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="9eb5f-323">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="9eb5f-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="9eb5f-324">AzureRM.Automation</span></span>
* <span data-ttu-id="9eb5f-325">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9eb5f-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9eb5f-326">AzureRM.Compute</span></span>
* <span data-ttu-id="9eb5f-327">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="9eb5f-328">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="9eb5f-329">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="9eb5f-330">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="9eb5f-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="9eb5f-331">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="9eb5f-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="9eb5f-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="9eb5f-333">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="9eb5f-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9eb5f-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9eb5f-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9eb5f-335">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="9eb5f-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="9eb5f-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="9eb5f-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="9eb5f-337">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="9eb5f-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9eb5f-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9eb5f-338">AzureRM.Network</span></span>
* <span data-ttu-id="9eb5f-339">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="9eb5f-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="9eb5f-340">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="9eb5f-341">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="9eb5f-342">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="9eb5f-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="9eb5f-343">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="9eb5f-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="9eb5f-344">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="9eb5f-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="9eb5f-345">AzureRM.Relay</span></span>
* <span data-ttu-id="9eb5f-346">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9eb5f-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9eb5f-347">AzureRM.Resources</span></span>
* <span data-ttu-id="9eb5f-348">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="9eb5f-349">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="9eb5f-350">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="9eb5f-351">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="9eb5f-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="9eb5f-352">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="9eb5f-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9eb5f-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9eb5f-354">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="9eb5f-355">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="9eb5f-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9eb5f-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="9eb5f-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9eb5f-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="9eb5f-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9eb5f-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="9eb5f-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9eb5f-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="9eb5f-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9eb5f-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="9eb5f-361">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="9eb5f-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="9eb5f-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9eb5f-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="9eb5f-363">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9eb5f-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9eb5f-364">AzureRM.Sql</span></span>
* <span data-ttu-id="9eb5f-365">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="9eb5f-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="9eb5f-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="9eb5f-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="9eb5f-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="9eb5f-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9eb5f-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9eb5f-368">AzureRM.Websites</span></span>
* <span data-ttu-id="9eb5f-369">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="9eb5f-370">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="9eb5f-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="9eb5f-371">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="9eb5f-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="9eb5f-372">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="9eb5f-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="9eb5f-373">一般</span><span class="sxs-lookup"><span data-stu-id="9eb5f-373">General</span></span>
* <span data-ttu-id="9eb5f-374">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="9eb5f-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="9eb5f-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9eb5f-375">AzureRM.Profile</span></span>
* <span data-ttu-id="9eb5f-376">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="9eb5f-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9eb5f-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9eb5f-377">AzureRM.Compute</span></span>
* <span data-ttu-id="9eb5f-378">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="9eb5f-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="9eb5f-379">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="9eb5f-380">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="9eb5f-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="9eb5f-381">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="9eb5f-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="9eb5f-382">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9eb5f-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="9eb5f-383">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="9eb5f-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="9eb5f-384">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9eb5f-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="9eb5f-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="9eb5f-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="9eb5f-386">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="9eb5f-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9eb5f-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="9eb5f-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9eb5f-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="9eb5f-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9eb5f-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9eb5f-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9eb5f-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9eb5f-391">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="9eb5f-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="9eb5f-392">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="9eb5f-393">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="9eb5f-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="9eb5f-394">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="9eb5f-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="9eb5f-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="9eb5f-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="9eb5f-396">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="9eb5f-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="9eb5f-397">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="9eb5f-398">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="9eb5f-399">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9eb5f-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9eb5f-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9eb5f-401">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="9eb5f-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9eb5f-402">AzureRM.Network</span></span>
* <span data-ttu-id="9eb5f-403">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="9eb5f-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="9eb5f-404">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="9eb5f-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="9eb5f-405">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="9eb5f-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="9eb5f-406">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="9eb5f-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="9eb5f-407">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="9eb5f-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="9eb5f-408">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="9eb5f-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="9eb5f-409">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="9eb5f-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="9eb5f-410">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="9eb5f-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="9eb5f-411">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="9eb5f-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="9eb5f-412">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="9eb5f-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="9eb5f-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9eb5f-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9eb5f-414">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="9eb5f-415">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="9eb5f-416">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9eb5f-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9eb5f-417">AzureRM.Resources</span></span>
* <span data-ttu-id="9eb5f-418">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="9eb5f-419">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="9eb5f-420">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="9eb5f-421">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="9eb5f-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="9eb5f-422">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="9eb5f-423">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="9eb5f-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="9eb5f-424">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="9eb5f-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="9eb5f-425">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="9eb5f-426">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="9eb5f-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="9eb5f-427">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="9eb5f-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="9eb5f-428">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="9eb5f-429">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="9eb5f-430">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="9eb5f-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="9eb5f-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="9eb5f-432">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9eb5f-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9eb5f-433">AzureRM.Sql</span></span>
* <span data-ttu-id="9eb5f-434">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="9eb5f-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="9eb5f-435">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="9eb5f-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="9eb5f-436">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="9eb5f-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9eb5f-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9eb5f-437">AzureRM.Profile</span></span>
* <span data-ttu-id="9eb5f-438">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="9eb5f-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="9eb5f-439">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="9eb5f-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="9eb5f-440">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-440">Azure.Storage</span></span>
* <span data-ttu-id="9eb5f-441">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9eb5f-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9eb5f-442">AzureRM.Compute</span></span>
* <span data-ttu-id="9eb5f-443">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="9eb5f-444">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="9eb5f-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="9eb5f-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="9eb5f-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9eb5f-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="9eb5f-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9eb5f-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="9eb5f-448">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="9eb5f-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb5f-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="9eb5f-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb5f-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="9eb5f-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb5f-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="9eb5f-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb5f-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="9eb5f-453">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="9eb5f-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="9eb5f-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9eb5f-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="9eb5f-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="9eb5f-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="9eb5f-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="9eb5f-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="9eb5f-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9eb5f-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="9eb5f-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9eb5f-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="9eb5f-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9eb5f-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="9eb5f-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9eb5f-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="9eb5f-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="9eb5f-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="9eb5f-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9eb5f-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="9eb5f-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="9eb5f-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="9eb5f-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="9eb5f-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="9eb5f-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="9eb5f-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="9eb5f-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9eb5f-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="9eb5f-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="9eb5f-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="9eb5f-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="9eb5f-469">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="9eb5f-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9eb5f-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9eb5f-471">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="9eb5f-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="9eb5f-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="9eb5f-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="9eb5f-473">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="9eb5f-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="9eb5f-474">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="9eb5f-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="9eb5f-475">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="9eb5f-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="9eb5f-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9eb5f-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="9eb5f-477">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="9eb5f-478">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9eb5f-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9eb5f-479">AzureRM.Sql</span></span>
* <span data-ttu-id="9eb5f-480">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="9eb5f-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9eb5f-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="9eb5f-482">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9eb5f-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9eb5f-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9eb5f-483">AzureRM.Websites</span></span>
* <span data-ttu-id="9eb5f-484">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="9eb5f-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="9eb5f-485">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="9eb5f-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="9eb5f-486">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="9eb5f-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="9eb5f-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="9eb5f-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="9eb5f-488">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="9eb5f-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="9eb5f-489">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="9eb5f-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9eb5f-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9eb5f-490">AzureRM.Profile</span></span>
* <span data-ttu-id="9eb5f-491">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="9eb5f-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="9eb5f-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="9eb5f-492">AzureRM.Compute</span></span>
* <span data-ttu-id="9eb5f-493">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="9eb5f-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="9eb5f-494">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="9eb5f-495">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="9eb5f-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9eb5f-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="9eb5f-497">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="9eb5f-498">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="9eb5f-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="9eb5f-499">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="9eb5f-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="9eb5f-500">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="9eb5f-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="9eb5f-501">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="9eb5f-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="9eb5f-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="9eb5f-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="9eb5f-503">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="9eb5f-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="9eb5f-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9eb5f-504">AzureRM.Network</span></span>
* <span data-ttu-id="9eb5f-505">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="9eb5f-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="9eb5f-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="9eb5f-506">AzureRM.Resources</span></span>
* <span data-ttu-id="9eb5f-507">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="9eb5f-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="9eb5f-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="9eb5f-509">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="9eb5f-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9eb5f-510">AzureRM.Sql</span></span>
* <span data-ttu-id="9eb5f-511">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9eb5f-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="9eb5f-512">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9eb5f-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="9eb5f-513">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9eb5f-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="9eb5f-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9eb5f-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="9eb5f-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9eb5f-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="9eb5f-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9eb5f-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="9eb5f-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="9eb5f-517">AzureRM.Websites</span></span>
* <span data-ttu-id="9eb5f-518">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="9eb5f-519">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="9eb5f-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="9eb5f-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9eb5f-520">AzureRM.Profile</span></span>
* <span data-ttu-id="9eb5f-521">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="9eb5f-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="9eb5f-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9eb5f-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="9eb5f-523">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="9eb5f-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9eb5f-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="9eb5f-525">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="9eb5f-526">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="9eb5f-527">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="9eb5f-528">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="9eb5f-529">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="9eb5f-530">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="9eb5f-531">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="9eb5f-531">Added support for MSI identity</span></span>
* <span data-ttu-id="9eb5f-532">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="9eb5f-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="9eb5f-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="9eb5f-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="9eb5f-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9eb5f-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="9eb5f-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="9eb5f-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="9eb5f-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="9eb5f-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="9eb5f-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="9eb5f-537">AzureRM.Batch</span></span>
* <span data-ttu-id="9eb5f-538">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="9eb5f-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="9eb5f-539">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="9eb5f-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="9eb5f-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="9eb5f-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="9eb5f-541">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="9eb5f-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="9eb5f-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="9eb5f-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="9eb5f-543">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="9eb5f-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="9eb5f-544">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="9eb5f-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="9eb5f-545">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="9eb5f-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="9eb5f-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="9eb5f-546">AzureRM.Network</span></span>
* <span data-ttu-id="9eb5f-547">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="9eb5f-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="9eb5f-548">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="9eb5f-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="9eb5f-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9eb5f-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="9eb5f-550">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="9eb5f-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9eb5f-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="9eb5f-552">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="9eb5f-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9eb5f-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="9eb5f-554">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="9eb5f-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="9eb5f-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9eb5f-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="9eb5f-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9eb5f-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="9eb5f-557">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="9eb5f-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="9eb5f-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="9eb5f-558">AzureRM.Sql</span></span>
* <span data-ttu-id="9eb5f-559">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="9eb5f-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="9eb5f-560">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="9eb5f-561">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="9eb5f-562">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="9eb5f-563">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="9eb5f-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="9eb5f-564">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9eb5f-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="9eb5f-565">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9eb5f-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="9eb5f-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9eb5f-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="9eb5f-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9eb5f-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="9eb5f-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9eb5f-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="9eb5f-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="9eb5f-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="9eb5f-570">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="9eb5f-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
