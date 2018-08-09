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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: afae9f2f091b21ed07d5aec1c249cf859a8b89a4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/09/2018
ms.locfileid: "39653486"
---
# <a name="release-notes"></a><span data-ttu-id="d384e-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="d384e-103">Release notes</span></span>

<span data-ttu-id="d384e-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="d384e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="d384e-105">6.6.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="d384e-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d384e-106">一般</span><span class="sxs-lookup"><span data-stu-id="d384e-106">General</span></span>
* <span data-ttu-id="d384e-107">已更新所有說明檔以包含完整的參數類型和正確的輸入/輸出類型。</span><span class="sxs-lookup"><span data-stu-id="d384e-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="d384e-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d384e-108">AzureRM.Profile</span></span>
* <span data-ttu-id="d384e-109">已更新 Common.Strategy 程式庫，以便能驗證資源目前的設定與目標資源相容。</span><span class="sxs-lookup"><span data-stu-id="d384e-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span> <span data-ttu-id="d384e-110">預設一律為 True，個別資源並覆寫預設。</span><span class="sxs-lookup"><span data-stu-id="d384e-110">Default is always true, individual resources and overridet the default.</span></span>
* <span data-ttu-id="d384e-111">已將 ps1xml 類型新增至 Common.Storage</span><span class="sxs-lookup"><span data-stu-id="d384e-111">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="d384e-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d384e-112">Azure.Storage</span></span>
* <span data-ttu-id="d384e-113">支援從 DefaulfProfile 取得儲存體內容</span><span class="sxs-lookup"><span data-stu-id="d384e-113">Support get Storage Context from DefaulfProfile</span></span>
* <span data-ttu-id="d384e-114">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性。</span><span class="sxs-lookup"><span data-stu-id="d384e-114">Add Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d384e-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d384e-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d384e-116">已修正的問題 https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="d384e-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="d384e-117">已修正 Automapper 中的錯誤，以將 PsApiManagementApi 轉譯為 ApiContract</span><span class="sxs-lookup"><span data-stu-id="d384e-117">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="d384e-118">已修正的問題 https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="d384e-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="d384e-119">已修正 File.Save 中的錯誤，不多載編碼類型</span><span class="sxs-lookup"><span data-stu-id="d384e-119">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="d384e-120">已修正的問題 https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="d384e-120">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="d384e-121">已升級至 4.0.3 Nuget 版本，其修正了 apiId 的模式例外狀況</span><span class="sxs-lookup"><span data-stu-id="d384e-121">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d384e-122">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d384e-122">AzureRM.Compute</span></span>
* <span data-ttu-id="d384e-123">修正因為重新命名 PremiumLRS 儲存體帳戶類型，而在 New-AzureRmVm 中使用 DiskFileParameterSet 建立 VM 失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="d384e-123">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="d384e-124">修正 Invoke-AzureRmVMRunCommand Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-124">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="d384e-125">更新 Get-AzureRmAvailabilitySet，以列出訂用帳戶中所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="d384e-125">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="d384e-126">(ResouceGroupName 參數現在為選用。)</span><span class="sxs-lookup"><span data-stu-id="d384e-126">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="d384e-127">更新 'New-AzureRmVm' 的 SimpleParameterSet，以在符合資格的 VM 上啟用加速網路。</span><span class="sxs-lookup"><span data-stu-id="d384e-127">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="d384e-128">更新 New-AzureRmVmss 簡單參數集，讓使用者指定的 LB 已存在時 vmss 建立會失敗。</span><span class="sxs-lookup"><span data-stu-id="d384e-128">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="d384e-129">更新 New-AzureRmDisk 的範例</span><span class="sxs-lookup"><span data-stu-id="d384e-129">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="d384e-130">新增 'New-AzureRmVM' 的範例</span><span class="sxs-lookup"><span data-stu-id="d384e-130">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="d384e-131">更新 Set-AzureRmVMOSDisk 的說明</span><span class="sxs-lookup"><span data-stu-id="d384e-131">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="d384e-132">更新 Set-AzureRmVMBginfoExtension 的範例 1 以更正拼字和前置詞。</span><span class="sxs-lookup"><span data-stu-id="d384e-132">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="d384e-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d384e-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="d384e-134">已將 ADF .Net SDK 版本更新為 1.1.0。</span><span class="sxs-lookup"><span data-stu-id="d384e-134">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="d384e-135">支援跨資料處理站的自我裝載整合執行階段共用。</span><span class="sxs-lookup"><span data-stu-id="d384e-135">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="d384e-136">新增新參數 -SharedIntegrationRuntimeResourceId 至 Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d384e-136">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="d384e-137">將新的選用參數 -LinkedDataFactoryName 新增至 Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d384e-137">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d384e-138">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d384e-138">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d384e-139">已將 DataPlane SDK (Microsoft.Azure.DataLake.Store) 版本更新為 1.1.9</span><span class="sxs-lookup"><span data-stu-id="d384e-139">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d384e-140">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d384e-140">AzureRM.EventHub</span></span>
* <span data-ttu-id="d384e-141">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="d384e-141">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="d384e-142">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="d384e-142">AzureRM.Insights</span></span>
* <span data-ttu-id="d384e-143">已修正說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="d384e-143">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="d384e-144">使用 Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="d384e-144">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d384e-145">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d384e-145">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d384e-146">修正 Set-AzureRmKeyVaultAccessPolicy 中的管線問題</span><span class="sxs-lookup"><span data-stu-id="d384e-146">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d384e-147">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d384e-147">AzureRM.Network</span></span>
* <span data-ttu-id="d384e-148">已新增 LoadBalancerInboundNatPoolConfig Cmdlet 的範例。</span><span class="sxs-lookup"><span data-stu-id="d384e-148">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d384e-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d384e-149">AzureRM.Resources</span></span>
* <span data-ttu-id="d384e-150">修正在提供 'Get-AzureRmResource' 標籤名稱和值時發生的問題</span><span class="sxs-lookup"><span data-stu-id="d384e-150">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="d384e-151">修正 'Set-AzureRmResource' 的管線狀況</span><span class="sxs-lookup"><span data-stu-id="d384e-151">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d384e-152">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d384e-152">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d384e-153">已在移除 Cmdlet 中更新了 InputObject 和 ResourceId 的管線</span><span class="sxs-lookup"><span data-stu-id="d384e-153">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="d384e-154">已修正一些問題</span><span class="sxs-lookup"><span data-stu-id="d384e-154">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="d384e-155">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d384e-155">AzureRM.Sql</span></span>
* <span data-ttu-id="d384e-156">透過下列 Cmdlet 新增伺服器進階威脅防護支援：</span><span class="sxs-lookup"><span data-stu-id="d384e-156">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="d384e-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d384e-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d384e-158">透過下列 Cmdlet 新增弱點評量支援：</span><span class="sxs-lookup"><span data-stu-id="d384e-158">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="d384e-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="d384e-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="d384e-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="d384e-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="d384e-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="d384e-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="d384e-162">已修正 Remove-AzureRmSqlServerFirewallRule 的範例</span><span class="sxs-lookup"><span data-stu-id="d384e-162">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="d384e-163">修正 Get-AzureSqlSyncGroupLog 中非美國文化不正確的日期時間處理方式</span><span class="sxs-lookup"><span data-stu-id="d384e-163">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="d384e-164">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="d384e-164">AzureRM.Storage</span></span>
* <span data-ttu-id="d384e-165">將 Ps1XmlAttribute 新增至 Cmdlet 輸出類型屬性</span><span class="sxs-lookup"><span data-stu-id="d384e-165">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="d384e-166">在資料表檢視中顯示 StorageAccount Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="d384e-166">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="d384e-167">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d384e-167">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="d384e-168">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d384e-168">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="d384e-169">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d384e-169">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="d384e-170">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="d384e-170">AzureRM.Tags</span></span>
* <span data-ttu-id="d384e-171">移除標籤 Cmdlet 說明中不正確的陳述式</span><span class="sxs-lookup"><span data-stu-id="d384e-171">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="d384e-172">6.5.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="d384e-172">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d384e-173">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d384e-173">AzureRM.Profile</span></span>
* <span data-ttu-id="d384e-174">已更新 'Get-AzureRmContextAutosaveSetting' 的說明</span><span class="sxs-lookup"><span data-stu-id="d384e-174">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="d384e-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d384e-175">Azure.Storage</span></span>
* <span data-ttu-id="d384e-176">支援使用唯寫 SAS 權杖上傳 Blob 或檔案</span><span class="sxs-lookup"><span data-stu-id="d384e-176">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="d384e-177">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d384e-177">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="d384e-178">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d384e-178">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="d384e-179">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d384e-179">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="d384e-180">將必要屬性 ResourceGroupName 新增至 AS。</span><span class="sxs-lookup"><span data-stu-id="d384e-180">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="d384e-181">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="d384e-181">AzureRM.Automation</span></span>
* <span data-ttu-id="d384e-182">針對 'New-AzureRMAutomationSchedule' 更新說明和新增範例</span><span class="sxs-lookup"><span data-stu-id="d384e-182">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d384e-183">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d384e-183">AzureRM.Compute</span></span>
* <span data-ttu-id="d384e-184">將 -Tag 參數新增至 Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d384e-184">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="d384e-185">新增 'Add-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="d384e-185">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="d384e-186">新增 'Remove-AzureRmVmssExtension' 的範例</span><span class="sxs-lookup"><span data-stu-id="d384e-186">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="d384e-187">更新 'Set-AzureRmVMAccessExtension' 的說明</span><span class="sxs-lookup"><span data-stu-id="d384e-187">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="d384e-188">針對 New-AzureRmVmss 更新 SimpleParameterSet，以將 SinglePlacementGroup 預設值設為 false，並且新增切換參數 'SinglePlacementGroup'，該參數可讓使用者在單一放置群組中建立 VMSS。</span><span class="sxs-lookup"><span data-stu-id="d384e-188">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d384e-189">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d384e-189">AzureRM.EventHub</span></span>
* <span data-ttu-id="d384e-190">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSEventHubDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="d384e-190">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d384e-191">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d384e-191">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d384e-192">更新 Set-AzureRmKeyVaultAccessPolicy 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="d384e-192">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="d384e-193">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d384e-193">AzureRM.LogicApp</span></span>
* <span data-ttu-id="d384e-194">已修正 New-AzureRmLogicApp 中的「無法解析參數集合」錯誤</span><span class="sxs-lookup"><span data-stu-id="d384e-194">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d384e-195">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d384e-195">AzureRM.Network</span></span>
* <span data-ttu-id="d384e-196">針對 Set/Add-AzureRmVirtualNetworkPeering 在多租用戶中的虛擬網路之間啟用對等互連</span><span class="sxs-lookup"><span data-stu-id="d384e-196">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="d384e-197">已更新應用程式閘道的下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-197">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="d384e-198">New-AzureRmApplicationGateway：已新增 EnableFIPS 旗標和區域支援</span><span class="sxs-lookup"><span data-stu-id="d384e-198">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="d384e-199">New-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="d384e-199">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="d384e-200">Set-AzureRmApplicationGatewaySku：已新增 SKU Standard_v2 和 WAF_v2</span><span class="sxs-lookup"><span data-stu-id="d384e-200">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="d384e-201">已使用最新的產生器版本重新產生 RouteTable Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-201">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="d384e-202">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="d384e-202">AzureRM.Relay</span></span>
* <span data-ttu-id="d384e-203">已更新 Markdown 檔案，修正範例中的參數名稱問題</span><span class="sxs-lookup"><span data-stu-id="d384e-203">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d384e-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d384e-204">AzureRM.Resources</span></span>
* <span data-ttu-id="d384e-205">更新 Roleassignment 和 roledefinition Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d384e-205">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="d384e-206">移除分頁時完成的額外 roledefinition 呼叫。</span><span class="sxs-lookup"><span data-stu-id="d384e-206">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="d384e-207">修正 Get-AzureRmRoleAssignment Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-207">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="d384e-208">修正 -ExpandPrincipalGroups 命令參數功能</span><span class="sxs-lookup"><span data-stu-id="d384e-208">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="d384e-209">修正 'Get-AzureRmResource' 中 '-ResourceType' 參數區分大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="d384e-209">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="d384e-210">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d384e-210">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d384e-211">已將 top 和 skip 參數新增至清單 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-211">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="d384e-212">已將標準新增至進階命名空間移轉 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d384e-212">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="d384e-213">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d384e-213">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d384e-214">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d384e-214">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d384e-215">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d384e-215">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d384e-216">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d384e-216">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="d384e-217">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d384e-217">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="d384e-218">已將唯讀屬性 'PendingReplicationOperationsCount' 新增至 PSServiceBusDRConfigurationAttributes 類別，如此會在複寫進行時給予擱置複寫作業計數</span><span class="sxs-lookup"><span data-stu-id="d384e-218">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d384e-219">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d384e-219">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d384e-220">更新 'New-AzureRmServiceFabricCluster' 的範例</span><span class="sxs-lookup"><span data-stu-id="d384e-220">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d384e-221">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d384e-221">AzureRM.Sql</span></span>
* <span data-ttu-id="d384e-222">新增 Management.Sql 的新 Cmdlet，以允許客戶將 TDE 憑證新增至 SQL Server 執行個體或受控執行個體</span><span class="sxs-lookup"><span data-stu-id="d384e-222">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="d384e-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d384e-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="d384e-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="d384e-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d384e-225">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d384e-225">AzureRM.Websites</span></span>
* <span data-ttu-id="d384e-226">`Set-AzureRmWebApp -AssignIdentity` 和 `Set-AzureRmWebAppSlot -AssignIdentity` 設為 false 時，現在也會從網站 object.Removing 預覽標記移除 Identity 屬性。</span><span class="sxs-lookup"><span data-stu-id="d384e-226">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="d384e-227">`Get-AzureRmWebAppMetrics`，`Get-AzureRmAppServicePlanMetrics` 範例已更新</span><span class="sxs-lookup"><span data-stu-id="d384e-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="d384e-228">`Set-AzureRmWebApp -PhpVersion` 支援有效的 PHP 版本</span><span class="sxs-lookup"><span data-stu-id="d384e-228">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="d384e-229">6.4.0 - 2018 年 7 月</span><span class="sxs-lookup"><span data-stu-id="d384e-229">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d384e-230">一般</span><span class="sxs-lookup"><span data-stu-id="d384e-230">General</span></span>
* <span data-ttu-id="d384e-231">已修正大部分模組說明檔案中的 OutputType 格式</span><span class="sxs-lookup"><span data-stu-id="d384e-231">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="d384e-232">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d384e-232">AzureRM.Profile</span></span>
* <span data-ttu-id="d384e-233">Ps1Xml 屬性已新增至基本輸出類型</span><span class="sxs-lookup"><span data-stu-id="d384e-233">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d384e-234">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d384e-234">AzureRM.Compute</span></span>
* <span data-ttu-id="d384e-235">VMSS 的 IP 標記功能</span><span class="sxs-lookup"><span data-stu-id="d384e-235">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="d384e-236">已新增 'New-AzureRmVmssIpTagConfig' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-236">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="d384e-237">IpTag 參數已新增至 New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="d384e-237">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="d384e-238">VMSS 的自動 OS 復原功能</span><span class="sxs-lookup"><span data-stu-id="d384e-238">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="d384e-239">DisableAutoRollback 參數已新增至 New-AzureRmVmssConfig 和 Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d384e-239">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="d384e-240">VMSS 的 OS 升級記錄功能</span><span class="sxs-lookup"><span data-stu-id="d384e-240">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="d384e-241">OSUpgradeHistory 參數已新增至 Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d384e-241">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="d384e-242">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d384e-242">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="d384e-243">透過下列命令，新增目錄 ACL 的支援：</span><span class="sxs-lookup"><span data-stu-id="d384e-243">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="d384e-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d384e-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="d384e-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d384e-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="d384e-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d384e-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d384e-247">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d384e-247">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d384e-248">新增 Set-AzureRmDataLakeStoreItemAclEntry、Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的取消支援和進度追蹤</span><span class="sxs-lookup"><span data-stu-id="d384e-248">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="d384e-249">新增 Export-AzureRmDataLakeStoreChildItemProperties 的取消支援</span><span class="sxs-lookup"><span data-stu-id="d384e-249">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="d384e-250">修正針對 Cmdlet (造成遞迴作業) 偵錯訊息進行排清</span><span class="sxs-lookup"><span data-stu-id="d384e-250">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="d384e-251">修正 DataLake Cmdlet 的測試位置</span><span class="sxs-lookup"><span data-stu-id="d384e-251">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="d384e-252">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="d384e-252">AzureRM.EventHub</span></span>
* <span data-ttu-id="d384e-253">將 Optional MaxCount 參數新增至清單作業 Cmdlet Get-AzureRmEventHub 和 Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d384e-253">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="d384e-254">已修正 New-AzureRmEventHub Cmdlet 在建立新 EventHub 時至少需要一個參數的問題。</span><span class="sxs-lookup"><span data-stu-id="d384e-254">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="d384e-255">提供預設參數集。</span><span class="sxs-lookup"><span data-stu-id="d384e-255">Provided Default Parameter set.</span></span>
* <span data-ttu-id="d384e-256">將選擇性參數 -KeyValue 新增至 New-AzureRmEventHubKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="d384e-256">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d384e-257">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d384e-257">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d384e-258">修正 Get-AzureRmKeyVault -Tag 傳回所有資源的問題</span><span class="sxs-lookup"><span data-stu-id="d384e-258">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="d384e-259">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d384e-259">AzureRM.Network</span></span>
* <span data-ttu-id="d384e-260">針對區域備援 VirtualNetworkGateways 公開新的 SKU</span><span class="sxs-lookup"><span data-stu-id="d384e-260">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="d384e-261">已透過 ARM 新增功能：ExpressRoute 合作夥伴 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="d384e-261">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="d384e-262">已新增 Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d384e-262">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="d384e-263">已新增 Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="d384e-263">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="d384e-264">已新增 Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d384e-264">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d384e-265">已新增 Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d384e-265">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d384e-266">已新增 Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="d384e-266">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="d384e-267">已新增 Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d384e-267">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d384e-268">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d384e-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d384e-269">已新增 Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d384e-269">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d384e-270">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d384e-270">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d384e-271">已新增 Get-AzureRmRecoveryServicesBackupStatus Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d384e-271">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="d384e-272">此 Cmdlet 會採用虛擬機器識別碼，並且檢查虛擬機器是否受到訂用帳戶中某些保存庫的保護。</span><span class="sxs-lookup"><span data-stu-id="d384e-272">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="d384e-273">如果有此類保存庫存在，Cmdlet 會輸出保存庫詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d384e-273">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d384e-274">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d384e-274">AzureRM.Resources</span></span>
* <span data-ttu-id="d384e-275">更新 Get-AzureRmPolicyAssignment Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="d384e-275">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="d384e-276">在管理群組層級新增清單 -Scope 值的支援</span><span class="sxs-lookup"><span data-stu-id="d384e-276">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="d384e-277">在管理群組層級新增對於使用 -Scope 值擷取個別指派的支援</span><span class="sxs-lookup"><span data-stu-id="d384e-277">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="d384e-278">將 -Effective 和 -All 參數新增至 control 參數</span><span class="sxs-lookup"><span data-stu-id="d384e-278">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="d384e-279">更新 Get/New/Remove/Set-AzureRmPolicyDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-279">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="d384e-280">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="d384e-280">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="d384e-281">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="d384e-281">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="d384e-282">更新 Get/New/Remove/Set-AzureRmPolicySetDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-282">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="d384e-283">新增 -ManagementGroupName 參數，以將作業套用至指定管理群組</span><span class="sxs-lookup"><span data-stu-id="d384e-283">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="d384e-284">新增 -SubscriptionId 參數，以將作業套用至指定訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="d384e-284">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="d384e-285">在 'New-AzureRmResourceGroupDeployment' 中使用 'TemplateParameterObject' 時，在參數中新增 KeyVault 秘密參考支援</span><span class="sxs-lookup"><span data-stu-id="d384e-285">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="d384e-286">修正針對 'New-AzureRmADAppCredential' 略過 '-EndDate' 參數的問題</span><span class="sxs-lookup"><span data-stu-id="d384e-286">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="d384e-287">修正 'Add-AzureRmADGroupMember' 使用了錯誤的 URL 提出要求的問題</span><span class="sxs-lookup"><span data-stu-id="d384e-287">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="d384e-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d384e-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="d384e-289">將選擇性參數 -KeyValue 新增至 New-AzureRmServiceBusKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="d384e-289">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d384e-290">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d384e-290">AzureRM.Sql</span></span>
* <span data-ttu-id="d384e-291">在 New-AzureRmSqlDatabaseRestorePoint 說明中釐清了 SQLDW 的使用者定義還原點</span><span class="sxs-lookup"><span data-stu-id="d384e-291">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="d384e-292">已在數個 Cmdlet 中更新 -ComputeGeneration 參數的文件</span><span class="sxs-lookup"><span data-stu-id="d384e-292">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="d384e-293">6.3.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="d384e-293">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d384e-294">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d384e-294">AzureRM.Profile</span></span>
* <span data-ttu-id="d384e-295">已更新的 Enable-AzureRmContextAutoSave 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="d384e-295">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="d384e-296">執行不包含先前內容的 'Connect-AzureRmAccount' 時，建立每個訂用帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="d384e-296">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="d384e-297">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d384e-297">Azure.Storage</span></span>
* <span data-ttu-id="d384e-298">在說明檔中新增了關於 -Permissions 參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="d384e-298">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d384e-299">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d384e-299">AzureRM.Compute</span></span>
* <span data-ttu-id="d384e-300">'Get-AzureRmVmDiskEncryptionStatus' 修正了沒有資料磁碟的 VM 所發生的問題</span><span class="sxs-lookup"><span data-stu-id="d384e-300">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="d384e-301">更新 Compute 用戶端程式庫版本來修正下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-301">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="d384e-302">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d384e-302">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="d384e-303">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="d384e-303">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="d384e-304">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="d384e-304">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="d384e-305">已修正下列 Cmdlet，以正確顯示「作業識別碼」和「作業狀態」：</span><span class="sxs-lookup"><span data-stu-id="d384e-305">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="d384e-306">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d384e-306">Start-AzureRmVM</span></span>
    - <span data-ttu-id="d384e-307">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d384e-307">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="d384e-308">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d384e-308">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="d384e-309">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d384e-309">Set-AzureRmVM</span></span>
    - <span data-ttu-id="d384e-310">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="d384e-310">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="d384e-311">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d384e-311">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="d384e-312">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="d384e-312">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="d384e-313">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="d384e-313">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="d384e-314">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d384e-314">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="d384e-315">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d384e-315">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="d384e-316">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d384e-316">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="d384e-317">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d384e-317">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="d384e-318">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d384e-318">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="d384e-319">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="d384e-319">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="d384e-320">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="d384e-320">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="d384e-321">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d384e-321">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="d384e-322">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="d384e-322">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="d384e-323">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d384e-323">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="d384e-324">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d384e-324">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="d384e-325">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d384e-325">AzureRM.EventGrid</span></span>
* <span data-ttu-id="d384e-326">將 Update-AzureRmEventGridSubscription Cmdlet 中 SubjectBeginsWith/SubjectEndsWith 的 ValidateNotNullOrEmpty 驗證條件移除，以允許視需要將這些參數變更為空白字串。</span><span class="sxs-lookup"><span data-stu-id="d384e-326">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="d384e-327">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d384e-327">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d384e-328">修正此問題：當 Get-AzureRmKeyVault -Tag 執行時，未傳回任何 Tag</span><span class="sxs-lookup"><span data-stu-id="d384e-328">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="d384e-329">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d384e-329">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="d384e-330">Policy Insights Cmdlet 的公開版本</span><span class="sxs-lookup"><span data-stu-id="d384e-330">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="d384e-331">使用 API 版本 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="d384e-331">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="d384e-332">將 PolicyDefinitionReferenceId 新增至 Get-AzureRmPolicyStateSummary 的結果中</span><span class="sxs-lookup"><span data-stu-id="d384e-332">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="d384e-333">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d384e-333">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d384e-334">已將 -Vault 參數新增至 RecoveryServices.Backup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d384e-334">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="d384e-335">當傳遞時，這會覆寫 Set-AzureRmRecoveryServicesContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d384e-335">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d384e-336">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d384e-336">AzureRM.Sql</span></span>
* <span data-ttu-id="d384e-337">說明檔中已更新的 Get-AzureRmSqlDatabaseExpanded 範例</span><span class="sxs-lookup"><span data-stu-id="d384e-337">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d384e-338">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d384e-338">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d384e-339">已更新說明檔的 Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d384e-339">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d384e-340">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d384e-340">AzureRM.Websites</span></span>
* <span data-ttu-id="d384e-341">'Set-AzureRmWebApp' 已更新為在使用 -AssignIdentity 時不會覆寫 AppSettings</span><span class="sxs-lookup"><span data-stu-id="d384e-341">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="d384e-342">'New-AzureRmWebAppSlot' 已更新為接受 AppServicePlan 作為選擇性參數</span><span class="sxs-lookup"><span data-stu-id="d384e-342">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="d384e-343">6.2.1 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="d384e-343">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="d384e-344">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d384e-344">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="d384e-345">已更新 PSWorkspace 模型，可允許 Network 使用 type 作為參數</span><span class="sxs-lookup"><span data-stu-id="d384e-345">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="d384e-346">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="d384e-346">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d384e-347">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d384e-347">AzureRM.Profile</span></span>
* <span data-ttu-id="d384e-348">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="d384e-348">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d384e-349">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d384e-349">AzureRM.Compute</span></span>
* <span data-ttu-id="d384e-350">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="d384e-350">VMSS VM Update feature</span></span>
    - <span data-ttu-id="d384e-351">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-351">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="d384e-352">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="d384e-352">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="d384e-353">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d384e-353">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="d384e-354">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="d384e-354">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="d384e-355">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="d384e-355">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="d384e-356">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="d384e-356">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="d384e-357">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="d384e-357">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="d384e-358">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="d384e-358">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="d384e-359">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d384e-359">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d384e-360">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="d384e-360">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="d384e-361">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d384e-361">AzureRM.Network</span></span>
* <span data-ttu-id="d384e-362">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="d384e-362">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d384e-363">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d384e-363">AzureRM.Resources</span></span>
* <span data-ttu-id="d384e-364">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="d384e-364">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="d384e-365">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="d384e-365">AzureRM.Scheduler</span></span>
* <span data-ttu-id="d384e-366">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="d384e-366">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="d384e-367">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d384e-367">AzureRM.Sql</span></span>
* <span data-ttu-id="d384e-368">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d384e-368">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="d384e-369">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d384e-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="d384e-370">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d384e-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="d384e-371">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d384e-371">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="d384e-372">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d384e-372">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="d384e-373">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d384e-373">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d384e-374">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d384e-374">AzureRM.Websites</span></span>
* <span data-ttu-id="d384e-375">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="d384e-375">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="d384e-376">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="d384e-376">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d384e-377">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="d384e-377">AzureRM.Profile</span></span>
* <span data-ttu-id="d384e-378">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="d384e-378">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="d384e-379">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d384e-379">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="d384e-380">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="d384e-380">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d384e-381">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d384e-381">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d384e-382">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="d384e-382">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="d384e-383">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="d384e-383">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="d384e-384">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="d384e-384">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="d384e-385">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="d384e-385">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="d384e-386">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="d384e-386">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="d384e-387">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="d384e-387">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="d384e-388">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="d384e-388">Added support for MSI identity</span></span>
* <span data-ttu-id="d384e-389">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="d384e-389">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="d384e-390">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="d384e-390">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="d384e-391">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d384e-391">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="d384e-392">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="d384e-392">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="d384e-393">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="d384e-393">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="d384e-394">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="d384e-394">AzureRM.Batch</span></span>
* <span data-ttu-id="d384e-395">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="d384e-395">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="d384e-396">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="d384e-396">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="d384e-397">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="d384e-397">AzureRM.Consumption</span></span>
* <span data-ttu-id="d384e-398">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="d384e-398">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d384e-399">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d384e-399">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d384e-400">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="d384e-400">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="d384e-401">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="d384e-401">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="d384e-402">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="d384e-402">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="d384e-403">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d384e-403">AzureRM.Network</span></span>
* <span data-ttu-id="d384e-404">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="d384e-404">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="d384e-405">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="d384e-405">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="d384e-406">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d384e-406">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="d384e-407">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="d384e-407">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="d384e-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d384e-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="d384e-409">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="d384e-409">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="d384e-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d384e-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="d384e-411">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="d384e-411">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="d384e-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d384e-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d384e-413">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d384e-413">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d384e-414">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="d384e-414">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d384e-415">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d384e-415">AzureRM.Sql</span></span>
* <span data-ttu-id="d384e-416">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="d384e-416">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="d384e-417">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="d384e-417">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="d384e-418">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="d384e-418">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="d384e-419">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="d384e-419">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="d384e-420">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="d384e-420">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="d384e-421">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d384e-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="d384e-422">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d384e-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="d384e-423">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d384e-423">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="d384e-424">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d384e-424">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="d384e-425">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d384e-425">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d384e-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d384e-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d384e-427">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="d384e-427">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>