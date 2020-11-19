---
title: Azure PowerShell 變更記錄
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 2/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: e6dd28596cdc4f18ddcd3de7886d222ed588caff
ms.sourcegitcommit: 6071038ed955107220a01156550a541bf68d0266
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/13/2020
ms.locfileid: "89243662"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="7e457-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="7e457-103">Azure PowerShell Release notes</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="7e457-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="7e457-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="azure-powershell-570"></a><span data-ttu-id="7e457-105">Azure PowerShell 5.7.0</span><span class="sxs-lookup"><span data-stu-id="7e457-105">Azure PowerShell 5.7.0</span></span>

<span data-ttu-id="7e457-106">Azure PowerShell 5.7.0 安裝程式：[連結](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)</span><span class="sxs-lookup"><span data-stu-id="7e457-106">Azure PowerShell 5.7.0 Installer: [link](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)</span></span>

<span data-ttu-id="7e457-107">適用於 ARM Cmdlet 的資源庫模組：[連結](https://www.powershellgallery.com/packages/AzureRM/5.7.0)</span><span class="sxs-lookup"><span data-stu-id="7e457-107">Gallery Module for ARM Cmdlets: [link](https://www.powershellgallery.com/packages/AzureRM/5.7.0)</span></span>

<span data-ttu-id="7e457-108">若要從 PowerShell 資源庫安裝 `AzureRM`，請執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="7e457-108">To install `AzureRM` from the PowerShell Gallery, run the following command:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -Repository PSGallery -Force
```

<span data-ttu-id="7e457-109">若要從舊版的 `AzureRM` 更新，請執行以下命令：</span><span class="sxs-lookup"><span data-stu-id="7e457-109">To update from an older version of `AzureRM`, run the following command:</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

### <a name="changes-since-last-release"></a><span data-ttu-id="7e457-110">自上次發行後的變更</span><span class="sxs-lookup"><span data-stu-id="7e457-110">Changes Since Last Release</span></span>

#### <a name="general"></a><span data-ttu-id="7e457-111">一般</span><span class="sxs-lookup"><span data-stu-id="7e457-111">General</span></span>
* <span data-ttu-id="7e457-112">已更新至最新版本的 Azure ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7e457-112">Updated to the latest version of the Azure ClientRuntime</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="7e457-113">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-113">Azure.Storage</span></span>
* <span data-ttu-id="7e457-114">修正在啟用 FIPS 原則的電腦上無法上傳 Blob 和檔案 Cmdlet 的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-114">Fix the issue that upload Blob and upload File cmdlets fail on FIPS policy enabled machines</span></span>
    - <span data-ttu-id="7e457-115">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7e457-115">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="7e457-116">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7e457-116">Set-AzureStorageFileContent</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="7e457-117">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="7e457-117">AzureRM.Billing</span></span>
* <span data-ttu-id="7e457-118">新 Cmdlet Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="7e457-118">New Cmdlet Get-AzureRmEnrollmentAccount</span></span>
  - <span data-ttu-id="7e457-119">擷取註冊帳戶的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-119">cmdlet to retrieve enrollment accounts</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="7e457-120">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e457-120">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="7e457-121">整合認知服務管理 SDK 4.0.0 版。</span><span class="sxs-lookup"><span data-stu-id="7e457-121">Integrate with Cognitive Services Management SDK version 4.0.0.</span></span>
* <span data-ttu-id="7e457-122">新增 Get-AzureRmCognitiveServicesAccountUsage 作業。</span><span class="sxs-lookup"><span data-stu-id="7e457-122">Add Get-AzureRmCognitiveServicesAccountUsage operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7e457-123">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7e457-123">AzureRM.Compute</span></span>
* <span data-ttu-id="7e457-124">`Get-AzureRmVmssDiskEncryptionStatus` 支援資料磁碟層級的加密狀態</span><span class="sxs-lookup"><span data-stu-id="7e457-124">`Get-AzureRmVmssDiskEncryptionStatus` supports encryption status at data disk level</span></span>
* <span data-ttu-id="7e457-125">`Get-AzureRmVmssVmDiskEncryptionStatus` 支援資料磁碟層級的加密狀態</span><span class="sxs-lookup"><span data-stu-id="7e457-125">`Get-AzureRmVmssVmDiskEncryptionStatus` supports encryption status at data disk level</span></span>
* <span data-ttu-id="7e457-126">更新以進行區域復原</span><span class="sxs-lookup"><span data-stu-id="7e457-126">Update for Zone Resilient</span></span>
* <span data-ttu-id="7e457-127">'New-AzureRmVm' 和 'New-AzureRmVmss' (簡單參數集全) 支援可用性區域。</span><span class="sxs-lookup"><span data-stu-id="7e457-127">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support availability zones.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="7e457-128">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e457-128">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="7e457-129">降低對 Commands.Resources.Rest 和 ARM/儲存體 SDK 的依賴。</span><span class="sxs-lookup"><span data-stu-id="7e457-129">Decouple reliance on Commands.Resources.Rest and ARM/Storage SDKs.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="7e457-130">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e457-130">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="7e457-131">新增偵錯功能</span><span class="sxs-lookup"><span data-stu-id="7e457-131">Add debug functionality</span></span>
* <span data-ttu-id="7e457-132">將 ADLS dataplane SDK 的版本更新至 1.1.2</span><span class="sxs-lookup"><span data-stu-id="7e457-132">Update the version of the ADLS dataplane SDK to 1.1.2</span></span>
* <span data-ttu-id="7e457-133">Export-AzureRmDataLakeStoreItem - 已取代 PerFileThreadCount、ConcurrentFileCount 參數並導入了參數並行</span><span class="sxs-lookup"><span data-stu-id="7e457-133">Export-AzureRmDataLakeStoreItem - Deprecated parameters PerFileThreadCount, ConcurrentFileCount and introduced parameter Concurrency</span></span>
* <span data-ttu-id="7e457-134">Import-AzureRMDataLakeStoreItem - 已取代 parametersPerFileThreadCount、ConcurrentFileCount 並導入了參數並行</span><span class="sxs-lookup"><span data-stu-id="7e457-134">Import-AzureRMDataLakeStoreItem - Deprecated parametersPerFileThreadCount, ConcurrentFileCount and introduced parameter Concurrency</span></span>
* <span data-ttu-id="7e457-135">Get-AzureRMDataLakeStoreItemContent - 已修正內容大於 4MB 的結尾行為</span><span class="sxs-lookup"><span data-stu-id="7e457-135">Get-AzureRMDataLakeStoreItemContent - Fixed the tail behavior for contents greater than 4MB</span></span>
* <span data-ttu-id="7e457-136">Set-AzureRMDataLakeStoreItemExpiry - 已導入新的參數集合 SetRelativeExpiry 以便設定相對的到期時間</span><span class="sxs-lookup"><span data-stu-id="7e457-136">Set-AzureRMDataLakeStoreItemExpiry - Introduced new parameter set SetRelativeExpiry for setting relative expiration time</span></span>
* <span data-ttu-id="7e457-137">Remove-AzureRmDataLakeStoreItem - 已取代 Clean 參數。</span><span class="sxs-lookup"><span data-stu-id="7e457-137">Remove-AzureRmDataLakeStoreItem - Deprecated parameter Clean.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="7e457-138">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e457-138">AzureRM.EventHub</span></span>
* <span data-ttu-id="7e457-139">已修正 New-AzureRmEventHubGeoDRConfiguration 中的 AlternameName</span><span class="sxs-lookup"><span data-stu-id="7e457-139">Fixed AlternameName in New-AzureRmEventHubGeoDRConfiguration</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="7e457-140">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e457-140">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7e457-141">已將 Cmdlet 更新為包含管線案例</span><span class="sxs-lookup"><span data-stu-id="7e457-141">Updated cmdlets to include piping scenarios</span></span>
* <span data-ttu-id="7e457-142">在即將推出的重大變更版本中新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="7e457-142">Add deprecation messages for upcoming breaking change release</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="7e457-143">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7e457-143">AzureRM.Network</span></span>
* <span data-ttu-id="7e457-144">使用 Network Cmdlet 修正錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="7e457-144">Fix error message with Network cmdlets</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="7e457-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e457-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="7e457-146">已在規則的 CorrelationFilter 中新增「屬性」，以便支援 CustomProperties</span><span class="sxs-lookup"><span data-stu-id="7e457-146">Added 'properties' in CorrelationFilter of Rules to support customproperties</span></span>
* <span data-ttu-id="7e457-147">已更新 New-AzureRmServiceBusGeoDRConfiguration 說明，並修正了規則 Cmdlet 輸出</span><span class="sxs-lookup"><span data-stu-id="7e457-147">updated New-AzureRmServiceBusGeoDRConfiguration help and fixed Rules cmdlet output</span></span>
* <span data-ttu-id="7e457-148">已修正 New-AzureRmServiceBusQueue 和 New-AzureRmServiceBusSubscription Cmdlet 中的自動轉送屬性</span><span class="sxs-lookup"><span data-stu-id="7e457-148">Fixed auto-forward properties in New-AzureRmServiceBusQueue and New-AzureRmServiceBusSubscription cmdlet</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7e457-149">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7e457-149">AzureRM.Sql</span></span>
* <span data-ttu-id="7e457-150">新增 Cmdlet 'Stop-AzureRmSqlElasticPoolActivity' 以支援在彈性集區中取消非同步作業</span><span class="sxs-lookup"><span data-stu-id="7e457-150">Add new cmdlet 'Stop-AzureRmSqlElasticPoolActivity' to support canceling the asynchronous operations on elastic pool</span></span>
* <span data-ttu-id="7e457-151">更新 Get-AzureRmSqlDatabaseActivity 和 Get-AzureRmSqlElasticPoolActivity Cmdlet 的回應，以在回應中反映更多資訊</span><span class="sxs-lookup"><span data-stu-id="7e457-151">Update the response for cmdlets Get-AzureRmSqlDatabaseActivity and Get-AzureRmSqlElasticPoolActivity to reflect more information in the response</span></span>

<span data-ttu-id="7e457-152">自上次發行後的變更： https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018</span><span class="sxs-lookup"><span data-stu-id="7e457-152">Changes since last release: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018</span></span>

## <a name="560---march-2018"></a><span data-ttu-id="7e457-153">5.6.0 - 2018 年 3 月</span><span class="sxs-lookup"><span data-stu-id="7e457-153">5.6.0 - March 2018</span></span>

#### <a name="general"></a><span data-ttu-id="7e457-154">一般</span><span class="sxs-lookup"><span data-stu-id="7e457-154">General</span></span>
* <span data-ttu-id="7e457-155">修正 CloudShell 中的預設資源群組問題</span><span class="sxs-lookup"><span data-stu-id="7e457-155">Fix issue with Default Resource Group in CloudShell</span></span>
* <span data-ttu-id="7e457-156">修正在模組匯入期間執行不正確啟動指令碼的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-156">Fix issue where incorrect startup scripts were being executed during module import</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="7e457-157">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7e457-157">AzureRM.Profile</span></span>
* <span data-ttu-id="7e457-158">在不支援的案例中啟用 MSI 驗證</span><span class="sxs-lookup"><span data-stu-id="7e457-158">Enable MSI authentication in unsupported scenarios</span></span>
* <span data-ttu-id="7e457-159">新增使用者定義的受控服務識別支援</span><span class="sxs-lookup"><span data-stu-id="7e457-159">Add support for user-defined Managed Service Identity</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="7e457-160">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e457-160">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="7e457-161">修正在組建中清理指令碼的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-161">Fixed issue with cleaning up scripts in build</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="7e457-162">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e457-162">AzureRM.Cdn</span></span>
* <span data-ttu-id="7e457-163">修正在組建中清理指令碼的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-163">Fixed issue with cleaning up scripts in build</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7e457-164">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7e457-164">AzureRM.Compute</span></span>
* <span data-ttu-id="7e457-165">'New-AzureRmVM' 和 'New-AzureRmVMSS' 支援資料磁碟機。</span><span class="sxs-lookup"><span data-stu-id="7e457-165">'New-AzureRmVM' and 'New-AzureRmVMSS' support data disks.</span></span>
* <span data-ttu-id="7e457-166">'New-AzureRmVM' 和 'New-AzureRmVMSS' 支援依名稱或識別碼的自訂映像。</span><span class="sxs-lookup"><span data-stu-id="7e457-166">'New-AzureRmVM' and 'New-AzureRmVMSS' support custom image by name or by id.</span></span>
* <span data-ttu-id="7e457-167">記錄分析功能</span><span class="sxs-lookup"><span data-stu-id="7e457-167">Log analytic feature</span></span>
    - <span data-ttu-id="7e457-168">已新增 'Export-AzureRmLogAnalyticRequestRateByInterval' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-168">Added 'Export-AzureRmLogAnalyticRequestRateByInterval' cmdlet</span></span>
    - <span data-ttu-id="7e457-169">已新增 'Export-AzureRmLogAnalyticThrottledRequests' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-169">Added 'Export-AzureRmLogAnalyticThrottledRequests' cmdlet</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="7e457-170">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7e457-170">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="7e457-171">修正登錄容器和 Azure 檔案磁碟區裝載的參數集問題</span><span class="sxs-lookup"><span data-stu-id="7e457-171">Fix parameter sets issue for container registry and azure file volume mount</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="7e457-172">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7e457-172">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="7e457-173">已將 ADF .Net SDK 更新為版本 0.6.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="7e457-173">Updated the ADF .Net SDK to version 0.6.0-preview containing the following changes:</span></span>
    - <span data-ttu-id="7e457-174">已新增新的 AzureDatabricks LinkedService 和 DatabricksNotebook 活動</span><span class="sxs-lookup"><span data-stu-id="7e457-174">Added new AzureDatabricks LinkedService and DatabricksNotebook Activity</span></span>
    - <span data-ttu-id="7e457-175">已在 HDInsightOnDemand LinkedService 中新增 headNodeSize 和 dataNodeSize 屬性</span><span class="sxs-lookup"><span data-stu-id="7e457-175">Added headNodeSize and dataNodeSize properties in HDInsightOnDemand LinkedService</span></span>
    - <span data-ttu-id="7e457-176">已為 SalesforceMarketingCloud 新增 LinkedService、Dataset、CopySource</span><span class="sxs-lookup"><span data-stu-id="7e457-176">Added LinkedService, Dataset, CopySource for SalesforceMarketingCloud</span></span>
    - <span data-ttu-id="7e457-177">已在所有活動上新增對 SecureOutput 的支援</span><span class="sxs-lookup"><span data-stu-id="7e457-177">Added support for SecureOutput on all activities</span></span>
    - <span data-ttu-id="7e457-178">已在 ForEach 新增新的 BatchCount 屬性，可控制要執行的並行活動數量</span><span class="sxs-lookup"><span data-stu-id="7e457-178">Added new BatchCount property on ForEach activity which control how many concurrent activities to run</span></span>
    - <span data-ttu-id="7e457-179">已新增新的篩選條件活動</span><span class="sxs-lookup"><span data-stu-id="7e457-179">Added new Filter Activity</span></span>
    - <span data-ttu-id="7e457-180">已新增連結服務參數的支援</span><span class="sxs-lookup"><span data-stu-id="7e457-180">Added Linked Service Parameters support</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="7e457-181">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="7e457-181">AzureRM.Dns</span></span>
* <span data-ttu-id="7e457-182">支援私人 DNS 區域 (公開預覽)</span><span class="sxs-lookup"><span data-stu-id="7e457-182">Support for Private DNS Zones (Public Preview)</span></span>
    - <span data-ttu-id="7e457-183">新增建立只有相關的虛擬網路才能看見的 DNS 區域之功能</span><span class="sxs-lookup"><span data-stu-id="7e457-183">Adds ability to create DNS zones that are visible only to the associated virtual networks</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="7e457-184">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7e457-184">AzureRM.Network</span></span>
* <span data-ttu-id="7e457-185">更新模型類型以與 DNS Cmdlet 相容。</span><span class="sxs-lookup"><span data-stu-id="7e457-185">Updating model types for compatibility with DNS cmdlets.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="7e457-186">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e457-186">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7e457-187">ASR Azure 到 Azure Site Recovery 的變更 (Cmdlet 目前支援企業到企業、企業到 Azure、HyperV 到 Azure 以及 VMware 到 Azure 的作業)</span><span class="sxs-lookup"><span data-stu-id="7e457-187">Changes for ASR Azure to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure,VMware to Azure)</span></span>
    - <span data-ttu-id="7e457-188">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7e457-188">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>
    - <span data-ttu-id="7e457-189">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="7e457-189">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>
    - <span data-ttu-id="7e457-190">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7e457-190">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>
    - <span data-ttu-id="7e457-191">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="7e457-191">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="7e457-192">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-192">AzureRM.Storage</span></span>
* <span data-ttu-id="7e457-193">新版本中已淘汰以下參數，並設定儲存體帳戶 Cmdlet：EnableEncryptionService 和 DisableEncryptionService，由於待用加密預設為已啟用且無法停用。</span><span class="sxs-lookup"><span data-stu-id="7e457-193">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="7e457-194">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e457-194">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="7e457-195">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e457-195">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="7e457-196">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7e457-196">AzureRM.Websites</span></span>
* <span data-ttu-id="7e457-197">已修正 Remove-AzureRmWebAppSlot 的說明</span><span class="sxs-lookup"><span data-stu-id="7e457-197">Fixed the help for Remove-AzureRmWebAppSlot</span></span>

## <a name="550---march-2018"></a><span data-ttu-id="7e457-198">5.5.0 - 2018 年 3 月</span><span class="sxs-lookup"><span data-stu-id="7e457-198">5.5.0 - March 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7e457-199">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7e457-199">AzureRM.Profile</span></span>
* <span data-ttu-id="7e457-200">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-200">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="7e457-201">與版本 6.0.8 並行載入 Newtonsoft.Json 版本 10.0.3</span><span class="sxs-lookup"><span data-stu-id="7e457-201">Load version 10.0.3 of Newtonsoft.Json side-by-side with version 6.0.8</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="7e457-202">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-202">Azure.Storage</span></span>
* <span data-ttu-id="7e457-203">支援虛刪除功能</span><span class="sxs-lookup"><span data-stu-id="7e457-203">Support Soft-Delete feature</span></span>
    - <span data-ttu-id="7e457-204">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e457-204">Enable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7e457-205">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7e457-205">Disable-AzureStorageDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7e457-206">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7e457-206">Get-AzureStorageBlob</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="7e457-207">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e457-207">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="7e457-208">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-208">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="7e457-209">新增防火牆和查詢向外延展功能的支援，並支援 2017-08-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="7e457-209">Add support of firewall and query scaleout feature, as well as support of 2017-08-01 api version.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="7e457-210">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="7e457-210">AzureRM.Automation</span></span>
* <span data-ttu-id="7e457-211">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-211">Fixed issue with importing aliases</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="7e457-212">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e457-212">AzureRM.Cdn</span></span>
* <span data-ttu-id="7e457-213">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-213">Fixed issue with importing aliases</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="7e457-214">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e457-214">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="7e457-215">更新 notice.txt 和通知訊息。</span><span class="sxs-lookup"><span data-stu-id="7e457-215">Update notice.txt and notice message.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7e457-216">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7e457-216">AzureRM.Compute</span></span>
* <span data-ttu-id="7e457-217">'New-AzureRmVMSS' 在詳細資訊模式中列印連接字串。</span><span class="sxs-lookup"><span data-stu-id="7e457-217">'New-AzureRmVMSS' prints connection strings in verbose mode.</span></span>
* <span data-ttu-id="7e457-218">'New-AzureRmVmss' 支援公用 IP 位址、載入平衡規則、傳入的 NAT 規則。</span><span class="sxs-lookup"><span data-stu-id="7e457-218">'New-AzureRmVmss' supports public IP address, load balancing rules, inbound NAT rules.</span></span>
* <span data-ttu-id="7e457-219">WriteAccelerator 功能</span><span class="sxs-lookup"><span data-stu-id="7e457-219">WriteAccelerator feature</span></span>
    - <span data-ttu-id="7e457-220">已將 WriteAccelerator 切換參數新增至下列 Cmdlet：Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="7e457-220">Added WriteAccelerator switch parameter to the following cmdlets: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk</span></span>
    - <span data-ttu-id="7e457-221">已將 OsDiskWriteAccelerator 切換參數新增至下列 Cmdlet：   Set-AzureRmVmssStorageProfile。</span><span class="sxs-lookup"><span data-stu-id="7e457-221">Added OsDiskWriteAccelerator switch parameter to the following cmdlet:     Set-AzureRmVmssStorageProfile.</span></span>
    - <span data-ttu-id="7e457-222">已將 OsDiskWriteAccelerator 布林值參數新增至下列 Cmdlet：   Update-AzureRmVM     Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="7e457-222">Added OsDiskWriteAccelerator Boolean parameter to the following cmdlets:     Update-AzureRmVM     Update-AzureRmVmss</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="7e457-223">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="7e457-223">AzureRM.DataFactories</span></span>
* <span data-ttu-id="7e457-224">修正會造成部分加密作業生產無意義錯誤的認證加密問題</span><span class="sxs-lookup"><span data-stu-id="7e457-224">Fix credential encryption issue that caused no meaningful error for some encryption operations</span></span>
* <span data-ttu-id="7e457-225">啟用要在資料處理站間共用的整合執行階段</span><span class="sxs-lookup"><span data-stu-id="7e457-225">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="7e457-226">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7e457-226">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="7e457-227">為 "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd 新增參數 "SetupScriptContainerSasUri" 和 "Edition"，以啟用自訂設定和編輯選項功能</span><span class="sxs-lookup"><span data-stu-id="7e457-227">Add parameter "SetupScriptContainerSasUri" and "Edition" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable custom setup and edition selection functionality</span></span>
* <span data-ttu-id="7e457-228">修正會造成部分加密作業生產無意義錯誤的認證加密問題。</span><span class="sxs-lookup"><span data-stu-id="7e457-228">Fix credential encryption issue that caused no meaningful error for some encryption operations.</span></span>
* <span data-ttu-id="7e457-229">啟用要在資料處理站間共用的整合執行階段</span><span class="sxs-lookup"><span data-stu-id="7e457-229">Enable integration runtime to be shared across data factory</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="7e457-230">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e457-230">AzureRM.HDInsight</span></span>
* <span data-ttu-id="7e457-231">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-231">Fixed issue with importing aliases</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="7e457-232">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e457-232">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7e457-233">已修正 Set-AzureRmKeyVaultAccessPolicy 範例</span><span class="sxs-lookup"><span data-stu-id="7e457-233">Fixed example for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="7e457-234">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7e457-234">AzureRM.Network</span></span>
* <span data-ttu-id="7e457-235">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-235">Fixed issue with importing aliases</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="7e457-236">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e457-236">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="7e457-237">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-237">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="7e457-238">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e457-238">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="7e457-239">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-239">Fixed issue with importing aliases</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="7e457-240">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e457-240">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7e457-241">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-241">Fixed issue with importing aliases</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="7e457-242">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7e457-242">AzureRM.Resources</span></span>
* <span data-ttu-id="7e457-243">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-243">Fixed issue with importing aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="7e457-244">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e457-244">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="7e457-245">已將 EnableBatchedOperations 屬性新增至佇列</span><span class="sxs-lookup"><span data-stu-id="7e457-245">Added EnableBatchedOperations property to Queue</span></span>
* <span data-ttu-id="7e457-246">已將 DeadLetteringOnFilterEvaluationExceptions 屬性新增至訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="7e457-246">Added DeadLetteringOnFilterEvaluationExceptions property to Subscriptions</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="7e457-247">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e457-247">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="7e457-248">Service Fabric Cmdlet 重新整理</span><span class="sxs-lookup"><span data-stu-id="7e457-248">Service Fabric cmdlet refresh</span></span>
  - <span data-ttu-id="7e457-249">已更新 ARM 範本</span><span class="sxs-lookup"><span data-stu-id="7e457-249">Updated ARM templates</span></span>
  - <span data-ttu-id="7e457-250">不再復原失敗的作業</span><span class="sxs-lookup"><span data-stu-id="7e457-250">Failed operations no longer rollback</span></span>
  - <span data-ttu-id="7e457-251">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="7e457-251">Add-AzureRmServiceFabricNodeType</span></span>
    - <span data-ttu-id="7e457-252">VM 預設位於受控磁碟</span><span class="sxs-lookup"><span data-stu-id="7e457-252">VMs default to managed disks</span></span>
    - <span data-ttu-id="7e457-253">使用現有的 VMSS 子網路</span><span class="sxs-lookup"><span data-stu-id="7e457-253">Existing VMSS subnet used</span></span>
    - <span data-ttu-id="7e457-254">均為等冪作業</span><span class="sxs-lookup"><span data-stu-id="7e457-254">All operations are idempotent</span></span>
  - <span data-ttu-id="7e457-255">Remove-AzureRmServiceFabricNodeType 會清除所立的部分 VMSS 和/或叢集節點類型</span><span class="sxs-lookup"><span data-stu-id="7e457-255">Remove-AzureRmServiceFabricNodeType cleans up partially created VMSS and/or cluster node types</span></span>
  - <span data-ttu-id="7e457-256">已修正複雜屬性類型的 PSCluster 物件輸出</span><span class="sxs-lookup"><span data-stu-id="7e457-256">Fixed output of PSCluster object for complex property types</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7e457-257">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7e457-257">AzureRM.Sql</span></span>
* <span data-ttu-id="7e457-258">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-258">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="7e457-259">Get-AzureRmSqlServer、New-AzureRmSqlServer 和 Remove-AzureRmSqlServer 回覆現在包括 FullyQualifiedDomainName 屬性。</span><span class="sxs-lookup"><span data-stu-id="7e457-259">Get-AzureRmSqlServer, New-AzureRmSqlServer, and Remove-AzureRmSqlServer response now includes FullyQualifiedDomainName property.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="7e457-260">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7e457-260">AzureRM.Websites</span></span>
* <span data-ttu-id="7e457-261">已修正匯入別名的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-261">Fixed issue with importing aliases</span></span>
* <span data-ttu-id="7e457-262">New-AzureRMWebApp - 已新增參數集供建立簡化 WebApp 之用，搭配本機 GIT 存放庫支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-262">New-AzureRMWebApp - added parameter set for simplified WebApp creation, with local git repository support.</span></span>

## <a name="540---february-2018"></a><span data-ttu-id="7e457-263">5.4.0 - 2018 年 2 月</span><span class="sxs-lookup"><span data-stu-id="7e457-263">5.4.0 - February 2018</span></span>
#### <a name="azurermautomation"></a><span data-ttu-id="7e457-264">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="7e457-264">AzureRM.Automation</span></span>
* <span data-ttu-id="7e457-265">將別名從 New-AzureRmAutomationModule 新增至 Import-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7e457-265">Added alias from New-AzureRmAutomationModule to Import-AzureRmAutomationModule</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7e457-266">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7e457-266">AzureRM.Compute</span></span>
* <span data-ttu-id="7e457-267">修正某些 Get Cmdlet 的 ErrorAction 問題。</span><span class="sxs-lookup"><span data-stu-id="7e457-267">Fix ErrorAction issue for some of Get cmdlets.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="7e457-268">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7e457-268">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="7e457-269">套用 Azure 容器執行個體 SDK 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="7e457-269">Apply Azure Container Instance SDK 2018-02-01</span></span>
    - <span data-ttu-id="7e457-270">支援 DNS 名稱標籤</span><span class="sxs-lookup"><span data-stu-id="7e457-270">Support DNS name label</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="7e457-271">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="7e457-271">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="7e457-272">修正所有先前未正常運作的 GET Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e457-272">Fixed all of the GET cmdlets which previously weren't working.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="7e457-273">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e457-273">AzureRM.EventHub</span></span>
* <span data-ttu-id="7e457-274">修正 Get-AzureRmEventHubGeoDRConfiguration 說明中的錯誤</span><span class="sxs-lookup"><span data-stu-id="7e457-274">Fix bug in Get-AzureRmEventHubGeoDRConfiguration help</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="7e457-275">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7e457-275">AzureRM.Network</span></span>
* <span data-ttu-id="7e457-276">已新增用來建立新連線監視的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-276">Added cmdlet to create a new connection monitor</span></span>
    - <span data-ttu-id="7e457-277">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7e457-277">New-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="7e457-278">已新增用來更新連線監視的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-278">Added cmdlet to update a connection monitor</span></span>
    - <span data-ttu-id="7e457-279">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7e457-279">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="7e457-280">已新增用來取得連線監視或連線監視清單的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-280">Added cmdlet to get connection monitor or connection monitor list</span></span>
    - <span data-ttu-id="7e457-281">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7e457-281">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="7e457-282">已新增用來查詢連線監視的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-282">Added cmdlet to query connection monitor</span></span>
    - <span data-ttu-id="7e457-283">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7e457-283">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>
* <span data-ttu-id="7e457-284">已新增用來啟動連線監視的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-284">Added cmdlet to start connection monitor</span></span>
    - <span data-ttu-id="7e457-285">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7e457-285">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="7e457-286">已新增用來停止連線監視的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-286">Added cmdlet to stop connection monitor</span></span>
    - <span data-ttu-id="7e457-287">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7e457-287">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="7e457-288">已新增用來移除連線監視的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-288">Added cmdlet to remove connection monitor</span></span>
    - <span data-ttu-id="7e457-289">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7e457-289">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>
* <span data-ttu-id="7e457-290">已更新 Set-AzureRmApplicationGatewayBackendAddressPool 文件從而移除已淘汰的範例</span><span class="sxs-lookup"><span data-stu-id="7e457-290">Updated Set-AzureRmApplicationGatewayBackendAddressPool documentation to remove deprecated example</span></span>
* <span data-ttu-id="7e457-291">已對應用程式閘道新增 EnableHttp2 旗標</span><span class="sxs-lookup"><span data-stu-id="7e457-291">Added EnableHttp2 flag to Application Gateway</span></span>
    - <span data-ttu-id="7e457-292">Updated New-AzureRmApplicationGateway：已新增選用參數 -EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="7e457-292">Updated New-AzureRmApplicationGateway: Added optional parameter -EnableHttp2</span></span>
* <span data-ttu-id="7e457-293">將 IpTags 新增至 PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e457-293">Add IpTags to PublicIpAddress</span></span>
    - <span data-ttu-id="7e457-294">更新了 New-AzureRmPublicIpAddress：已新增 IpTags</span><span class="sxs-lookup"><span data-stu-id="7e457-294">Updated New-AzureRmPublicIpAddress: Added IpTags</span></span>
    - <span data-ttu-id="7e457-295">New-AzureRmPublicIpTag 以新增 Iptag</span><span class="sxs-lookup"><span data-stu-id="7e457-295">New-AzureRmPublicIpTag to add Iptag</span></span>
* <span data-ttu-id="7e457-296">在 RouteTable 和 effectiveRoute 中新增 DisableBgpRoutePropagation 屬性。</span><span class="sxs-lookup"><span data-stu-id="7e457-296">Add DisableBgpRoutePropagation property in RouteTable and effectiveRoute.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="7e457-297">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7e457-297">AzureRM.Resources</span></span>
* <span data-ttu-id="7e457-298">Register-AzureRmProviderFeature：已在文件中新增遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="7e457-298">Register-AzureRmProviderFeature: Added missing example in the docs</span></span>
* <span data-ttu-id="7e457-299">Register-AzureRmResourceProvider：已在文件中新增遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="7e457-299">Register-AzureRmResourceProvider: Added missing example in the docs</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="7e457-300">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-300">AzureRM.Storage</span></span>
* <span data-ttu-id="7e457-301">新版本中已淘汰以下參數，並設定儲存體帳戶 Cmdlet：EnableEncryptionService 和 DisableEncryptionService，由於待用加密預設為已啟用且無法停用。</span><span class="sxs-lookup"><span data-stu-id="7e457-301">Obsolete following parameters in new and set Storage Account cmdlets: EnableEncryptionService and DisableEncryptionService, since Encryption at Rest is enabled by default and can't be disabled.</span></span>
    - <span data-ttu-id="7e457-302">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e457-302">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="7e457-303">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e457-303">Set-AzureRmStorageAccount</span></span>


## <a name="530---february-2018"></a><span data-ttu-id="7e457-304">5.3.0 - 2018 年 2 月</span><span class="sxs-lookup"><span data-stu-id="7e457-304">5.3.0 - February 2018</span></span>
### <a name="azurermprofile"></a><span data-ttu-id="7e457-305">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7e457-305">AzureRM.Profile</span></span>
* <span data-ttu-id="7e457-306">已新增 PowerShell 3 和 4 的取代警告</span><span class="sxs-lookup"><span data-stu-id="7e457-306">Added deprecation warning for PowerShell 3 and 4</span></span>
* <span data-ttu-id="7e457-307">`Add-AzureRmAccount` 已重新命名為 `Connect-AzureRmAccount`；舊的 Cmdlet 名稱已新增別名，而其他別名 (`Login-AzAccount` 和 `Login-AzureRmAccount`) 已重新導向至新的 Cmdlet 名稱。</span><span class="sxs-lookup"><span data-stu-id="7e457-307">`Add-AzureRmAccount` has been renamed as `Connect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Login-AzAccount` and `Login-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="7e457-308">`Remove-AzureRmAccount` 已重新命名為 `Disconnect-AzureRmAccount`；舊的 Cmdlet 名稱已新增別名，而其他別名 (`Logout-AzAccount` 和 `Logout-AzureRmAccount`) 已重新導向至新的 Cmdlet 名稱。</span><span class="sxs-lookup"><span data-stu-id="7e457-308">`Remove-AzureRmAccount` has been renamed as `Disconnect-AzureRmAccount`; an alias has been added for the old cmdlet name, and other aliases (`Logout-AzAccount` and `Logout-AzureRmAccount`) have been redirected to the new cmdlet name.</span></span>
* <span data-ttu-id="7e457-309">已更正資源字串使用 `Connect-AzureRmAccount`，而不是 `Login-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="7e457-309">Corrected Resource Strings to use `Connect-AzureRmAccount` instead of `Login-AzureRmAccount`</span></span>
* <span data-ttu-id="7e457-310">`Add-AzureRmEnvironment` 和 `Set-AzureRmEnvironment`</span><span class="sxs-lookup"><span data-stu-id="7e457-310">`Add-AzureRmEnvironment` and `Set-AzureRmEnvironment`</span></span>
  - <span data-ttu-id="7e457-311">已將 `-AzureOperationalInsightsEndpoint` 和 `-AzureOperationalInsightsEndpointResourceId`新增為參數，搭配 OperationalInsights 資料平面 RP 使用。</span><span class="sxs-lookup"><span data-stu-id="7e457-311">Added `-AzureOperationalInsightsEndpoint` and `-AzureOperationalInsightsEndpointResourceId` as parameters for use with OperationalInsights data plane RP.</span></span>

### <a name="azurermanalysisservices"></a><span data-ttu-id="7e457-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e457-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="7e457-313">已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="7e457-313">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="7e457-314">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7e457-314">AzureRM.Compute</span></span>
* <span data-ttu-id="7e457-315">已將 `-AvailabilitySetName` 參數新增至簡化的 `New-AzureRmVM` 參數集。</span><span class="sxs-lookup"><span data-stu-id="7e457-315">Added `-AvailabilitySetName` parameter to the simplified parameterset of `New-AzureRmVM`.</span></span>
* <span data-ttu-id="7e457-316">已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="7e457-316">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="7e457-317">適用於 VM 和 VM 擴展集的使用者指派識別身分支援</span><span class="sxs-lookup"><span data-stu-id="7e457-317">User assigned identity support for VM and VM scale set</span></span>
    - <span data-ttu-id="7e457-318">已將 `-IdentityType` 和 `-IdentityId` 參數新增至 `New-AzureRmVMConfig`、`New-AzureRmVmssConfig`、`Update-AzureRmVM` 和 `Update-AzureRmVmss`</span><span class="sxs-lookup"><span data-stu-id="7e457-318">`-IdentityType` and `-IdentityId` parameters are added to `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` and `Update-AzureRmVmss`</span></span>
* <span data-ttu-id="7e457-319">在 `Add-AzureRmVmssNetworkInterfaceConfig` 中新增 `-EnableIPForwarding` 參數</span><span class="sxs-lookup"><span data-stu-id="7e457-319">Added `-EnableIPForwarding` parameter to `Add-AzureRmVmssNetworkInterfaceConfig`</span></span>
* <span data-ttu-id="7e457-320">在 `New-AzureRmVmssConfig` 中新增 `-Priority` 參數</span><span class="sxs-lookup"><span data-stu-id="7e457-320">Added `-Priority` parameter to `New-AzureRmVmssConfig`</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="7e457-321">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e457-321">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="7e457-322">已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="7e457-322">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="7e457-323">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e457-323">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="7e457-324">已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="7e457-324">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>
* <span data-ttu-id="7e457-325">已更正執行此 Cmdlet 而不需要登入 `Login-AzureRmAccount` 時的 `Test-AzureRmDataLakeStoreAccount` 錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="7e457-325">Corrected the error message of `Test-AzureRmDataLakeStoreAccount` when running this cmdlet without having logged in with `Login-AzureRmAccount`</span></span>

### <a name="azurermeventgrid"></a><span data-ttu-id="7e457-326">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7e457-326">AzureRM.EventGrid</span></span>
* <span data-ttu-id="7e457-327">已更新使用 2018-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="7e457-327">Updated to use the 2018-01-01 API version.</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="7e457-328">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e457-328">AzureRM.EventHub</span></span>

* <span data-ttu-id="7e457-329">已新增下列異地災害復原作業的新命令。</span><span class="sxs-lookup"><span data-stu-id="7e457-329">Added below new commands for Geo Disaster Recovery operations.</span></span>
  - <span data-ttu-id="7e457-330">建立新的別名 (災害復原設定)：</span><span class="sxs-lookup"><span data-stu-id="7e457-330">Creating a new Alias (Disaster Recovery configuration):</span></span>
    - `New-AzureRmEventHubGeoDRConfiguration`
  - <span data-ttu-id="7e457-331">擷取別名 (災害復原設定)：</span><span class="sxs-lookup"><span data-stu-id="7e457-331">Retrieve Alias (Disaster Recovery configuration) :</span></span>
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - <span data-ttu-id="7e457-332">停用災害復原，並停止將變更從主要命名空間複寫至次要命名空間</span><span class="sxs-lookup"><span data-stu-id="7e457-332">Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - <span data-ttu-id="7e457-333">叫用災害復原容錯移轉，並將別名重新設定為指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="7e457-333">Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace</span></span>
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - <span data-ttu-id="7e457-334">刪除別名 (災害復原設定)</span><span class="sxs-lookup"><span data-stu-id="7e457-334">Deleting an Alias(Disaster Recovery configuration)</span></span>
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* <span data-ttu-id="7e457-335">已新增下列命令，用以檢查命名空間名稱和 GeoDr 設定名稱 - 別名可用性。</span><span class="sxs-lookup"><span data-stu-id="7e457-335">Added below new commands for checking the Namespace Name and GeoDr Configuration Name - Alias availability.</span></span>
  - <span data-ttu-id="7e457-336">檢查命名空間名稱或別名 (災害復原設定) 名稱的可用性：</span><span class="sxs-lookup"><span data-stu-id="7e457-336">Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name:</span></span>
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a><span data-ttu-id="7e457-337">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="7e457-337">AzureRM.Insights</span></span>
* <span data-ttu-id="7e457-338">已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="7e457-338">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="7e457-339">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e457-339">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7e457-340">已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="7e457-340">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="7e457-341">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7e457-341">AzureRM.Network</span></span>
* <span data-ttu-id="7e457-342">修正覆寫訊息「您確定要覆寫來源嗎」</span><span class="sxs-lookup"><span data-stu-id="7e457-342">Fix overwrite message 'Are you sure you want to overwriteresource'</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="7e457-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e457-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="7e457-344">已新增透過 `Invoke-AzureRmOperationalInsightsQuery` 進行 V2 API 查詢的支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-344">Added support for V2 API querying via `Invoke-AzureRmOperationalInsightsQuery`.</span></span> <span data-ttu-id="7e457-345">請參閱 [https://dev.loganalytics.io/](https://dev.loganalytics.io/) 以取得新 API 的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7e457-345">See [https://dev.loganalytics.io/](https://dev.loganalytics.io/) for more info on the new API.</span></span>

### <a name="azurermresources"></a><span data-ttu-id="7e457-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7e457-346">AzureRM.Resources</span></span>
* <span data-ttu-id="7e457-347">`Get-AzureRmADServicePrincipal`:已將 `-ServicePrincipalName` 從預設的空參數集移除，因為它是多餘的 SPN 參數集</span><span class="sxs-lookup"><span data-stu-id="7e457-347">`Get-AzureRmADServicePrincipal`: Removed `-ServicePrincipalName` from the default Empty parameter set as it was redundant with the SPN parameter set</span></span>

### <a name="azurermservicebus"></a><span data-ttu-id="7e457-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e457-348">AzureRM.ServiceBus</span></span>

* <span data-ttu-id="7e457-349">已新增 `Remove-AzureRmServiceBusRule` 和 `Get-AzureRmServiceBusKey` 的功能修正</span><span class="sxs-lookup"><span data-stu-id="7e457-349">Added functionality fix for `Remove-AzureRmServiceBusRule` and `Get-AzureRmServiceBusKey`</span></span>
* <span data-ttu-id="7e457-350">已新增下列異地災害復原作業的新 Commandlet。</span><span class="sxs-lookup"><span data-stu-id="7e457-350">Added below new commandlets for Geo Disaster Recovery operations.</span></span>
  - <span data-ttu-id="7e457-351">建立新的別名 (災害復原設定)：</span><span class="sxs-lookup"><span data-stu-id="7e457-351">Creating a new Alias (Disaster Recovery configuration):</span></span>
    - `New-AzureRmServiceBusDRConfigurations`
  - <span data-ttu-id="7e457-352">擷取別名 (災害復原設定)：</span><span class="sxs-lookup"><span data-stu-id="7e457-352">Retrieve Alias (Disaster Recovery configuration) :</span></span>
    - `Get-AzureRmServiceBusDRConfigurations`
  - <span data-ttu-id="7e457-353">停用災害復原，並停止將變更從主要命名空間複寫至次要命名空間</span><span class="sxs-lookup"><span data-stu-id="7e457-353">Disabling the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - <span data-ttu-id="7e457-354">叫用災害復原容錯移轉，並將別名重新設定為指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="7e457-354">Invoking Disaster Recovery failover and reconfigure the alias to point to the secondary namespace</span></span>
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - <span data-ttu-id="7e457-355">刪除別名 (災害復原設定)</span><span class="sxs-lookup"><span data-stu-id="7e457-355">Deleting an Alias(Disaster Recovery configuration)</span></span>
    - `Remove-AzureRmServiceBusDRConfigurations`
* <span data-ttu-id="7e457-356">已更新 `Test-AzureRmServiceBusName` Commandlet 以支援異地災害復原 - 別名名稱檢查可用性作業。</span><span class="sxs-lookup"><span data-stu-id="7e457-356">Updated `Test-AzureRmServiceBusName` commandlets to support Geo Disaster Recovery - Alias name check availability operations.</span></span>
  - <span data-ttu-id="7e457-357">檢查命名空間名稱或別名 (災害復原設定) 名稱的可用性：</span><span class="sxs-lookup"><span data-stu-id="7e457-357">Check the Availability of Namespace name or Alias(Disaster Recovery configuration) name:</span></span>
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a><span data-ttu-id="7e457-358">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="7e457-358">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="7e457-359">已更正 `Login-AzureRmAccount` 的使用方式來使用 `Connect-AzureRmAccount`</span><span class="sxs-lookup"><span data-stu-id="7e457-359">Corrected usage of `Login-AzureRmAccount` to use `Connect-AzureRmAccount`</span></span>

## <a name="520---january-2018"></a><span data-ttu-id="7e457-360">5.2.0 - 2018 年 1 月</span><span class="sxs-lookup"><span data-stu-id="7e457-360">5.2.0 - January 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="7e457-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="7e457-361">AzureRM.Profile</span></span>
* <span data-ttu-id="7e457-362">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-362">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-363">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="7e457-363">Add-AzureRmAccount</span></span>
  * <span data-ttu-id="7e457-364">已新增 -MSI 登入，以便使用目前虛擬機器/服務的受管理服務身分識別之認證來進行驗證</span><span class="sxs-lookup"><span data-stu-id="7e457-364">Added -MSI login for authenticationg using the credentials of the Managed Service Identity of the current VM / Service</span></span>
  * <span data-ttu-id="7e457-365">修正了以使用者所提供的存取權杖登入時，KeyVault 驗證所發生的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-365">Fixed KeyVault Authentication when logging in with user-provided access tokens</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="7e457-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-366">Azure.Storage</span></span>
* <span data-ttu-id="7e457-367">新增用以取得和設定儲存體服務屬性的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-367">Add cmdlets to get and set Storage service properties</span></span>
    - <span data-ttu-id="7e457-368">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7e457-368">Get-AzureStorageServiceProperty</span></span>
    - <span data-ttu-id="7e457-369">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7e457-369">Update-AzureStorageServiceProperty</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="7e457-370">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e457-370">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="7e457-371">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-371">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="7e457-372">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e457-372">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="7e457-373">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-373">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-374">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-374">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-375">針對 New-AzureRmApiManagementProperty、Set-AzureRmApiManagementProperty 和 New-AzureRmApiManagement，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-375">Obsoleted -Tags in favor of -Tag for New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty, and New-AzureRmApiManagement</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="7e457-376">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7e457-376">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="7e457-377">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-377">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-378">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-378">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="7e457-379">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="7e457-379">AzureRM.Automation</span></span>
* <span data-ttu-id="7e457-380">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-380">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-381">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-381">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-382">針對 Set-AzureRmAutomationRunbook，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-382">Obsoleted -Tags in favor of -Tag for Set-AzureRmAutomationRunbook</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="7e457-383">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="7e457-383">AzureRM.Backup</span></span>
* <span data-ttu-id="7e457-384">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-384">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-385">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-385">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="7e457-386">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="7e457-386">AzureRM.Batch</span></span>
* <span data-ttu-id="7e457-387">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-387">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-388">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-388">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="7e457-389">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="7e457-389">AzureRM.Cdn</span></span>
* <span data-ttu-id="7e457-390">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-390">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-391">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-391">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-392">針對 New-AzureRmCdnEndpoint 和 New-AzureRmCdnProfile，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-392">Obsoleted -Tags in favor of -Tag for New-AzureRmCdnEndpoint and New-AzureRmCdnProfile</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="7e457-393">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7e457-393">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="7e457-394">整合認知服務管理 SDK 3.0.0 版。</span><span class="sxs-lookup"><span data-stu-id="7e457-394">Integrate with Cognitive Services Management SDK version 3.0.0.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="7e457-395">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7e457-395">AzureRM.Compute</span></span>
* <span data-ttu-id="7e457-396">已將簡化的參數新增到 New-AzureRmVmss，後者會使用智慧型預設值建立虛擬機器擴展集和所有必要的資源</span><span class="sxs-lookup"><span data-stu-id="7e457-396">Added simplified parameter set to New-AzureRmVmss, which creates a Virtual Machine Scale Set and all required resources using smart defaults</span></span>
* <span data-ttu-id="7e457-397">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-397">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-398">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-398">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-399">針對 New-AzureRmVm 和 Update-AzureRmVm，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-399">Obsoleted -Tags in favor of -Tag for New-AzureRmVm and Update-AzureRmVm</span></span>
* <span data-ttu-id="7e457-400">修正了限制中包含區域時，Get-AzureRmComputeResourceSku Cmdlet 所發生的問題。</span><span class="sxs-lookup"><span data-stu-id="7e457-400">Fixed Get-AzureRmComputeResourceSku cmdlet when Zone is included in restriction.</span></span>
* <span data-ttu-id="7e457-401">為了支援 Azure 監視器的接收，已更新診斷代理程式的設定結構描述。</span><span class="sxs-lookup"><span data-stu-id="7e457-401">Updated Diagnostics Agent configuration schema for Azure Monitor sink support.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="7e457-402">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7e457-402">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="7e457-403">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-403">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-404">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-404">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="7e457-405">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e457-405">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="7e457-406">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-406">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-407">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-407">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="7e457-408">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="7e457-408">AzureRM.DataFactories</span></span>
* <span data-ttu-id="7e457-409">已讓所有資料存放區所連結的服務都支援 Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="7e457-409">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="7e457-410">已新增 Azure SSIS 整合執行階段的授權類型屬性</span><span class="sxs-lookup"><span data-stu-id="7e457-410">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="7e457-411">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-411">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-412">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-412">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-413">針對 New-AzureRmDataFactory，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-413">Obsoleted -Tags in favor of -Tag for New-AzureRmDataFactory</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="7e457-414">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7e457-414">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="7e457-415">已讓所有資料存放區所連結的服務都支援 Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="7e457-415">Enabled Azure Key Vault support for all data store linked services</span></span>
* <span data-ttu-id="7e457-416">已新增 Azure SSIS 整合執行階段的授權類型屬性</span><span class="sxs-lookup"><span data-stu-id="7e457-416">Added license type property for Azure SSIS integration runtime</span></span>
* <span data-ttu-id="7e457-417">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-417">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-418">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-418">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-419">新增「Set-AzureRmDataFactoryV2IntegrationRuntime」cmd 的參數「LicenseType」以啟用 AHUB 功能</span><span class="sxs-lookup"><span data-stu-id="7e457-419">Add parameter "LicenseType" for "Set-AzureRmDataFactoryV2IntegrationRuntime" cmd to enable AHUB functionality</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="7e457-420">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e457-420">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="7e457-421">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-421">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-422">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-422">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-423">針對 AzureRmDataLakeAnalyticsAccount 和 Set-AzureRmDataLakeAnalyticsAccount，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-423">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeAnalyticsAccount and Set-AzureRmDataLakeAnalyticsAccount</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="7e457-424">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e457-424">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="7e457-425">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-425">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-426">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-426">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-427">針對 New-AzureRmDataLakeStoreAccount 和 Set-AzureRmDataLakeStoreAccount，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-427">Obsoleted -Tags in favor of -Tag for New-AzureRmDataLakeStoreAccount and Set-AzureRmDataLakeStoreAccount</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="7e457-428">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="7e457-428">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="7e457-429">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-429">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="7e457-430">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="7e457-430">AzureRM.Dns</span></span>
* <span data-ttu-id="7e457-431">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-431">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="7e457-432">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7e457-432">AzureRM.EventGrid</span></span>
* <span data-ttu-id="7e457-433">已新增下列的新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="7e457-433">Added the following new cmdlet:</span></span>
  - <span data-ttu-id="7e457-434">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7e457-434">Update-AzureRmEventGridSubscription</span></span>
    - <span data-ttu-id="7e457-435">更新 Event Grid 事件訂閱的屬性。</span><span class="sxs-lookup"><span data-stu-id="7e457-435">Update the properties of an Event Grid event subscription.</span></span>
* <span data-ttu-id="7e457-436">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-436">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-437">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-437">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="7e457-438">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="7e457-438">AzureRM.EventHub</span></span>
* <span data-ttu-id="7e457-439">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-439">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-440">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-440">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="7e457-441">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e457-441">AzureRM.HDInsight</span></span>
* <span data-ttu-id="7e457-442">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-442">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-443">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-443">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="7e457-444">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="7e457-444">AzureRM.Insights</span></span>
* <span data-ttu-id="7e457-445">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-445">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-446">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-446">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="7e457-447">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="7e457-447">AzureRM.IotHub</span></span>
* <span data-ttu-id="7e457-448">新增 IoTHub Cmdlet 的憑證支援</span><span class="sxs-lookup"><span data-stu-id="7e457-448">Add Certificate support for IoTHub cmdlets</span></span>
* <span data-ttu-id="7e457-449">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-449">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-450">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-450">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="7e457-451">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e457-451">AzureRM.KeyVault</span></span>
* <span data-ttu-id="7e457-452">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-452">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-453">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-453">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-454">已針對長時間執行的 KeyVault Cmdlet 新增 -AsJob 支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-454">Added -AsJob support for long-running KeyVault cmdlets.</span></span> <span data-ttu-id="7e457-455">允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。</span><span class="sxs-lookup"><span data-stu-id="7e457-455">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
  * <span data-ttu-id="7e457-456">受影響的 cmdlet 為：Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="7e457-456">Affected cmdlet is: Remove-AzureRmKeyVault</span></span>
* <span data-ttu-id="7e457-457">修正了 Set-AzureRmKeyVaultAccessPolicy 中，AAD 篩選器會將 SPN 設為提供的 UPN 而非設定 UPN 本身的錯誤</span><span class="sxs-lookup"><span data-stu-id="7e457-457">Fixed bug in Set-AzureRmKeyVaultAccessPolicy where the AAD filter was setting SPN to the provided UPN, rather than setting the UPN</span></span>
  - <span data-ttu-id="7e457-458">請參閱下列問題以取得更多資訊： https://github.com/Azure/azure-powershell/issues/5201</span><span class="sxs-lookup"><span data-stu-id="7e457-458">See the following issue for more information: https://github.com/Azure/azure-powershell/issues/5201</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="7e457-459">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7e457-459">AzureRM.LogicApp</span></span>
* <span data-ttu-id="7e457-460">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-460">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-461">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-461">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="7e457-462">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7e457-462">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="7e457-463">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-463">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-464">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-464">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-465">針對 Update-AzureRmMlCommitmentPlan，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-465">Obsoleted -Tags in favor of -Tag for Update-AzureRmMlCommitmentPlan</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="7e457-466">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7e457-466">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="7e457-467">將 IncludeAllResources 參數新增到 Remove-AzureRmMlOpCluster Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-467">Add IncludeAllResources parameter to Remove-AzureRmMlOpCluster cmdlet</span></span>
  - <span data-ttu-id="7e457-468">使用此切換參數，將移除原本與叢集一起建立的所有資源</span><span class="sxs-lookup"><span data-stu-id="7e457-468">Using this switch parameter will remove all resources that were created with the cluster originally</span></span>
* <span data-ttu-id="7e457-469">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-469">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-470">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-470">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="7e457-471">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="7e457-471">AzureRM.Media</span></span>
* <span data-ttu-id="7e457-472">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-472">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-473">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-473">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-474">針對 Set-AzureRmMediaService 和 New-AzureRmMediaService，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-474">Obsoleted -Tags in favor of -Tag for Set-AzureRmMediaService and New-AzureRmMediaService</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="7e457-475">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="7e457-475">AzureRM.Network</span></span>
* <span data-ttu-id="7e457-476">已針對長時間執行的 Network Cmdlet 新增 -AsJob 支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-476">Added -AsJob support for long-running Network cmdlets.</span></span> <span data-ttu-id="7e457-477">允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。</span><span class="sxs-lookup"><span data-stu-id="7e457-477">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="7e457-478">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-478">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-479">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-479">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="7e457-480">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7e457-480">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="7e457-481">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-481">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-482">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-482">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-483">針對 New-AzureRmNotificationHubsNamespace 和 Set-AzureRmNotificationHubsNamespace，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-483">Obsoleted -Tags in favor of -Tag for New-AzureRmNotificationHubsNamespace and Set-AzureRmNotificationHubsNamespace</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="7e457-484">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7e457-484">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="7e457-485">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-485">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-486">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-486">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-487">針對 New-AzureRmOperationalInsightsSavedSearch、Set-AzureRmOperationalInsightsSavedSearch、New-AzureRmOperationalInsightsWorkspace 和 Set-AzureRmOperationalInsightsWorkspace，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-487">Obsoleted -Tags in favor of -Tag for New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspace, and Set-AzureRmOperationalInsightsWorkspace</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="7e457-488">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7e457-488">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="7e457-489">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-489">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-490">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-490">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="7e457-491">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e457-491">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="7e457-492">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-492">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-493">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-493">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="7e457-494">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7e457-494">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7e457-495">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-495">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-496">已將 -UseOriginalStorageAccount 選項新增到 Restore-AzureRmRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e457-496">Added -UseOriginalStorageAccount option to the Restore-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>
  - <span data-ttu-id="7e457-497">啟用此旗標會將磁碟還原到原始的儲存體帳戶，這可讓使用者將所還原虛擬機器的設定，盡可能重設回原始虛擬機器的設定。</span><span class="sxs-lookup"><span data-stu-id="7e457-497">Enabling this flag results in restoring disks to their original storage accounts which allows users to maintain the configuration of restored VM as close to the original VMs as possible.</span></span>
  - <span data-ttu-id="7e457-498">這也有助於改善還原作業的效能。</span><span class="sxs-lookup"><span data-stu-id="7e457-498">It also helps in improving the performance of the restore operation.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="7e457-499">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7e457-499">AzureRM.RedisCache</span></span>
* <span data-ttu-id="7e457-500">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-500">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-501">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-501">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-502">已新增 3 個防火牆規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-502">Added  3 new cmdlets for firewall rules</span></span>
* <span data-ttu-id="7e457-503">已新增 3 個異地複寫的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-503">Added  3 new cmdlets for geo replication</span></span>
* <span data-ttu-id="7e457-504">已新增區域和標籤的支援</span><span class="sxs-lookup"><span data-stu-id="7e457-504">Added support for zones and tags</span></span>
* <span data-ttu-id="7e457-505">盡可能將 ResourceGroup 設為選用。</span><span class="sxs-lookup"><span data-stu-id="7e457-505">Make ResourceGroup as optional whenever possible.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="7e457-506">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="7e457-506">AzureRM.Relay</span></span>
* <span data-ttu-id="7e457-507">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-507">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-508">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-508">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="7e457-509">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="7e457-509">AzureRM.Resources</span></span>
* <span data-ttu-id="7e457-510">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-510">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-511">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-511">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-512">已針對長時間執行的 Resources Cmdlet 新增 -AsJob 支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-512">Added -AsJob support for long-running Resources cmdlets.</span></span> <span data-ttu-id="7e457-513">允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。</span><span class="sxs-lookup"><span data-stu-id="7e457-513">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
* <span data-ttu-id="7e457-514">已從 Get-AzureRmProviderOperation 新增別名到 Get-AzureRmResourceProviderAction 以符合命名慣例</span><span class="sxs-lookup"><span data-stu-id="7e457-514">Added alias from Get-AzureRmProviderOperation to Get-AzureRmResourceProviderAction to conform with naming conventions</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="7e457-515">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="7e457-515">AzureRM.Scheduler</span></span>
* <span data-ttu-id="7e457-516">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-516">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-517">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-517">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservermanagement"></a><span data-ttu-id="7e457-518">AzureRM.ServerManagement</span><span class="sxs-lookup"><span data-stu-id="7e457-518">AzureRM.ServerManagement</span></span>
* <span data-ttu-id="7e457-519">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-519">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-520">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-520">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-521">針對 New-AzureRmServerManagementNode 和 New-AzureRmServerManagementGateway，已淘汰 -Tags 並改用 -Tag</span><span class="sxs-lookup"><span data-stu-id="7e457-521">Obsoleted -Tags in favor of -Tag for New-AzureRmServerManagementNode and New-AzureRmServerManagementGateway</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="7e457-522">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e457-522">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="7e457-523">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-523">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-524">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-524">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="7e457-525">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7e457-525">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="7e457-526">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-526">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-527">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-527">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsiterecovery"></a><span data-ttu-id="7e457-528">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e457-528">AzureRM.SiteRecovery</span></span>
* <span data-ttu-id="7e457-529">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-529">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-530">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-530">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="7e457-531">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7e457-531">AzureRM.Sql</span></span>
* <span data-ttu-id="7e457-532">更新 Auditing 命令參數描述</span><span class="sxs-lookup"><span data-stu-id="7e457-532">Update the Auditing commands parameters description</span></span>
* <span data-ttu-id="7e457-533">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-533">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-534">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-534">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-535">已將 -AsJob 參數新增到長時間執行的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-535">Added -AsJob parameter to long running cmdlets</span></span>
* <span data-ttu-id="7e457-536">已從 Get-AzureRmSqlServiceObjective 中淘汰了 -DatabaseName 參數</span><span class="sxs-lookup"><span data-stu-id="7e457-536">Obsoleted -DatabaseName parameter from Get-AzureRmSqlServiceObjective</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="7e457-537">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-537">AzureRM.Storage</span></span>
* <span data-ttu-id="7e457-538">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-538">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-539">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-539">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-540">修正了以參數 -EnableEncryptionService None 執行 Cmdlet New-AzureRMStorageAccount 時，所發生的 null 參考問題</span><span class="sxs-lookup"><span data-stu-id="7e457-540">Fix a null reference issue of run cmdlet New-AzureRMStorageAccount with parameter -EnableEncryptionService None</span></span>
* <span data-ttu-id="7e457-541">已針對長時間執行的 Storage Cmdlet 新增 -AsJob 支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-541">Added -AsJob support for long-running Storage cmdlets.</span></span> <span data-ttu-id="7e457-542">允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。</span><span class="sxs-lookup"><span data-stu-id="7e457-542">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="7e457-543">受影響的 Cmdlet 是適用於儲存體帳戶和儲存體帳戶網路規則的 New-、Remove-、Add- 和 Update-。</span><span class="sxs-lookup"><span data-stu-id="7e457-543">Affected cmdlets are New-, Remove-, Add-, and Update- for Storage Account and Storage Account Network Rule.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="7e457-544">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e457-544">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="7e457-545">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-545">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-546">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-546">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="7e457-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7e457-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="7e457-548">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-548">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-549">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-549">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="7e457-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="7e457-550">AzureRM.Websites</span></span>
* <span data-ttu-id="7e457-551">已將 Location 完成碼新增到 -Location 參數中，以便透過有效的位置來實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-551">Added Location Completer to -Location parameters allowing tab completion through valid Locations</span></span>
* <span data-ttu-id="7e457-552">已將 ResourceGroup 完成碼新增到 -ResourceGroup 參數中，以便在目前的訂用帳戶中透過資源群組實現 Tab 鍵自動完成</span><span class="sxs-lookup"><span data-stu-id="7e457-552">Added ResourceGroup Completer to -ResourceGroup parameters allowing tab completion through resource groups in current subscription</span></span>
* <span data-ttu-id="7e457-553">已針對長時間執行的 Websites Cmdlet 新增 -AsJob 支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-553">Added -AsJob support for long-running Websites cmdlets.</span></span> <span data-ttu-id="7e457-554">允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。</span><span class="sxs-lookup"><span data-stu-id="7e457-554">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
     - <span data-ttu-id="7e457-555">WebApps、AppServicePlan 和 Slots中，受影響的 Cmdlet 是 New-、Remove-、Add- 和 Set-</span><span class="sxs-lookup"><span data-stu-id="7e457-555">Affected cmdlets are New-, Remove-, Add-, and Set- for WebApps, AppServicePlan and Slots</span></span>

## <a name="2017128-version-511"></a><span data-ttu-id="7e457-556">2017.12.8 版本 5.1.1</span><span class="sxs-lookup"><span data-stu-id="7e457-556">2017.12.8 Version 5.1.1</span></span>
* <span data-ttu-id="7e457-557">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e457-557">AnalysisServices</span></span>
  - <span data-ttu-id="7e457-558">將位置的驗證集變更為動態對應，以便支援所有雲端。</span><span class="sxs-lookup"><span data-stu-id="7e457-558">Change validate set of location to dynamic lookup so that all clouds are supported.</span></span>
* <span data-ttu-id="7e457-559">自動化</span><span class="sxs-lookup"><span data-stu-id="7e457-559">Automation</span></span>
  - <span data-ttu-id="7e457-560">更新至 Import-AzureRMAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e457-560">Update to Import-AzureRMAutomationRunbook</span></span>
    - <span data-ttu-id="7e457-561">現在可支援 Python2 Runbook</span><span class="sxs-lookup"><span data-stu-id="7e457-561">Support is now being provided for Python2 runbooks</span></span>
* <span data-ttu-id="7e457-562">Batch</span><span class="sxs-lookup"><span data-stu-id="7e457-562">Batch</span></span>
  - <span data-ttu-id="7e457-563">修正錯誤：不含資源群組的帳戶作業無法自動偵測資源群組</span><span class="sxs-lookup"><span data-stu-id="7e457-563">Fixed a bug where account operations without a resource group failed to auto-detect the resource group</span></span>
* <span data-ttu-id="7e457-564">計算</span><span class="sxs-lookup"><span data-stu-id="7e457-564">Compute</span></span>
  - <span data-ttu-id="7e457-565">Get-AzureRmComputeResourceSku 會顯示區域資訊。</span><span class="sxs-lookup"><span data-stu-id="7e457-565">Get-AzureRmComputeResourceSku shows zone information.</span></span>
  - <span data-ttu-id="7e457-566">更新 Disable-AzureRmVmssDiskEncryption 以修正問題 https://github.com/Azure/azure-powershell/issues/5038</span><span class="sxs-lookup"><span data-stu-id="7e457-566">Update Disable-AzureRmVmssDiskEncryption to fix issue https://github.com/Azure/azure-powershell/issues/5038</span></span>
  - <span data-ttu-id="7e457-567">針對長時間執行的計算 Cmdlet 新增 -AsJob 支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-567">Added -AsJob support for long-running Compute cmdlets.</span></span> <span data-ttu-id="7e457-568">允許選取的 Cmdlet 在背景中執行，並傳回作業以追蹤及控制進度。</span><span class="sxs-lookup"><span data-stu-id="7e457-568">Allows selected cmdlets to run in the background and return a job to track and control progress.</span></span>
    - <span data-ttu-id="7e457-569">受影響的 cmdlet 包括：適用於虛擬機器和虛擬機器擴展集的 New-、Update-、Set-、Remove-、Start-、Restart- 和 Stop- Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-569">Affected cmdlets include: New-, Update-, Set-, Remove-, Start-, Restart-, Stop- cmdlets for Virtual Machines and Virtual Machine Scale Sets</span></span>
    - <span data-ttu-id="7e457-570">將簡化的參數集新增至 New-AzureRmVM，New-AzureRmVM 可使用智慧型預設值建立虛擬機器和所有必要的資源</span><span class="sxs-lookup"><span data-stu-id="7e457-570">Added simplified parameter set to New-AzureRmVM, which creates a Virtual Machine and all required resources using smart defaults</span></span>
* <span data-ttu-id="7e457-571">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7e457-571">ContainerInstance</span></span>
  - <span data-ttu-id="7e457-572">套用 Azure 容器執行個體 SDK 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="7e457-572">Apply Azure Container Instance SDK 2017-10-01</span></span>
    - <span data-ttu-id="7e457-573">支援容器的「執行到完成」作業</span><span class="sxs-lookup"><span data-stu-id="7e457-573">Support container run-to-completion</span></span>
    - <span data-ttu-id="7e457-574">支援 Azure 檔案磁碟區掛接</span><span class="sxs-lookup"><span data-stu-id="7e457-574">Support Azure File volume mount</span></span>
    - <span data-ttu-id="7e457-575">支援開啟多個公用 IP 的連接埠</span><span class="sxs-lookup"><span data-stu-id="7e457-575">Support opening multiple ports for public IP</span></span>
* <span data-ttu-id="7e457-576">ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e457-576">ContainerRegistry</span></span>
  - <span data-ttu-id="7e457-577">新增異地複寫與 Webhook 的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-577">New cmdlets for geo-replication and webhooks</span></span>
    - <span data-ttu-id="7e457-578">Get/New/Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="7e457-578">Get/New/Remove-AzureRmContainerRegistryReplication</span></span>
    - <span data-ttu-id="7e457-579">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7e457-579">Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook</span></span>
* <span data-ttu-id="7e457-580">DataFactories</span><span class="sxs-lookup"><span data-stu-id="7e457-580">DataFactories</span></span>
    - <span data-ttu-id="7e457-581">認證加密功能現在可與啟用的「遠端存取」(透過網路) 和停用的「遠端存取」(本機電腦) 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="7e457-581">Credential encryption functionality now works with both "Remote Access" enabled (Over Network) and "Remote Access" disabled (Local Machine).</span></span>
* <span data-ttu-id="7e457-582">DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7e457-582">DataFactoryV2</span></span>
  - <span data-ttu-id="7e457-583">已新增兩個新的 Cmdlet：Update-AzureRmDataFactoryV2 和 Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="7e457-583">Added two new cmdlets: Update-AzureRmDataFactoryV2 and Stop-AzureRmDataFactoryV2PipelineRun</span></span>
* <span data-ttu-id="7e457-584">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e457-584">DataLakeAnalytics</span></span>
  - <span data-ttu-id="7e457-585">將名為 ScriptParameter 的參數新增至 Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e457-585">Added a parameter called ScriptParameter to Submit-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="7e457-586">可在 Submit-AzureRmDataLakeAnalyticsJob 上使用 Get-help 找到 ScriptParameter 的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="7e457-586">Detailed information about ScriptParameter can be found using Get-Help on Submit-AzureRmDataLakeAnalyticsJob</span></span>
  - <span data-ttu-id="7e457-587">針對 New-AzureRmDataLakeAnalyticsAccount，已將參數 MaxDegreeOfParallelism 變更為 MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="7e457-587">For New-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
    - <span data-ttu-id="7e457-588">新增參數 MaxAnalyticsUnits 的別名：MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="7e457-588">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
  - <span data-ttu-id="7e457-589">針對 New-AzureRmDataLakeAnalyticsComputePolicy，已將參數 MaxDegreeOfParallelismPerJob 變更為 MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="7e457-589">For New-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
    - <span data-ttu-id="7e457-590">新增參數 MaxAnalyticsUnitsPerJob 的別名：MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="7e457-590">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
  - <span data-ttu-id="7e457-591">針對 Set-AzureRmDataLakeAnalyticsAccount，已將參數 MaxDegreeOfParallelism 變更為 MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="7e457-591">For Set-AzureRmDataLakeAnalyticsAccount, changed the parameter MaxDegreeOfParallelism to MaxAnalyticsUnits</span></span>
    - <span data-ttu-id="7e457-592">新增參數 MaxAnalyticsUnits 的別名：MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="7e457-592">Added an alias for the parameter MaxAnalyticsUnits: MaxDegreeOfParallelism</span></span>
  - <span data-ttu-id="7e457-593">針對 Submit-AzureRmDataLakeAnalyticsJob，已將參數 DegreeOfParallelism 變更為 AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="7e457-593">For Submit-AzureRmDataLakeAnalyticsJob, changed the parameter DegreeOfParallelism to AnalyticsUnits</span></span>
    - <span data-ttu-id="7e457-594">新增參數 AnalyticsUnits 的別名：DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="7e457-594">Added an alias for the parameter AnalyticsUnits: DegreeOfParallelism</span></span>
  - <span data-ttu-id="7e457-595">針對 Update-AzureRmDataLakeAnalyticsComputePolicy，已將參數 MaxDegreeOfParallelismPerJob 變更為 MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="7e457-595">For Update-AzureRmDataLakeAnalyticsComputePolicy, changed the parameter MaxDegreeOfParallelismPerJob to MaxAnalyticsUnitsPerJob</span></span>
    - <span data-ttu-id="7e457-596">新增參數 MaxAnalyticsUnitsPerJob 的別名：MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="7e457-596">Added an alias for the parameter MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob</span></span>
* <span data-ttu-id="7e457-597">MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7e457-597">MachineLearningCompute</span></span>
  - <span data-ttu-id="7e457-598">新增 Set-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7e457-598">Add Set-AzureRmMlOpCluster</span></span>
    - <span data-ttu-id="7e457-599">更新叢集的代理程式計數或 SSL 設定</span><span class="sxs-lookup"><span data-stu-id="7e457-599">Update a cluster's agent count or SSL configuration</span></span>
  - <span data-ttu-id="7e457-600">協調器屬性是選擇性項目</span><span class="sxs-lookup"><span data-stu-id="7e457-600">Orchestrator properties are optional</span></span>
    - <span data-ttu-id="7e457-601">服務會建立服務主體 (如果未提供的話)，因此協調器屬性現在是選擇性項目</span><span class="sxs-lookup"><span data-stu-id="7e457-601">The service will create a service principal if not provided, so the orchestrator properties are now optional</span></span>
* <span data-ttu-id="7e457-602">PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7e457-602">PowerBIEmbedded</span></span>
  - <span data-ttu-id="7e457-603">新增 Power BI Embedded 容量 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="7e457-603">Add support for Power BI Embedded Capacity cmdlets</span></span>
  - <span data-ttu-id="7e457-604">新增 Get-AzureRmPowerBIEmbeddedCapacity Cmdlet - 取得 PowerBI Embedded 容量的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7e457-604">New Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - Gets the details of a PowerBI Embedded Capacity.</span></span>
  - <span data-ttu-id="7e457-605">新增 New-AzureRmPowerBIEmbeddedCapacity Cmdlet - 建立新的 PowerBI Embedded 容量</span><span class="sxs-lookup"><span data-stu-id="7e457-605">New Cmdlet New-AzureRmPowerBIEmbeddedCapacity - Creates a new PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="7e457-606">新增 Remove-AzureRmPowerBIEmbeddedCapacity Cmdlet - 刪除 PowerBI Embedded 容量的執行個體</span><span class="sxs-lookup"><span data-stu-id="7e457-606">New Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - Deletes an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="7e457-607">新增 Resume-AzureRmPowerBIEmbeddedCapacity Cmdlet - 恢復 PowerBI Embedded 容量的執行個體</span><span class="sxs-lookup"><span data-stu-id="7e457-607">New Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - Resumes an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="7e457-608">新增 Suspend-AzureRmPowerBIEmbeddedCapacity Cmdlet - 暫止 PowerBI Embedded 容量的執行個體</span><span class="sxs-lookup"><span data-stu-id="7e457-608">New Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - Suspends an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="7e457-609">新增 Test-AzureRmPowerBIEmbeddedCapacity Cmdlet - 測試 PowerBI Embedded 容量執行個體是否存在</span><span class="sxs-lookup"><span data-stu-id="7e457-609">New Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - Tests the existence of an instance of PowerBI Embedded Capacity</span></span>
  - <span data-ttu-id="7e457-610">新增 Update-AzureRmPowerBIEmbeddedCapacity Cmdlet - 修改 PowerBI Embedded 容量的執行個體</span><span class="sxs-lookup"><span data-stu-id="7e457-610">New Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - Modifies an instance of PowerBI Embedded Capacity</span></span>
* <span data-ttu-id="7e457-611">設定檔</span><span class="sxs-lookup"><span data-stu-id="7e457-611">Profile</span></span>
  - <span data-ttu-id="7e457-612">已將 USGovernmentActiveDirectoryEndpoint 更新為 https://login.microsoftonline.us/</span><span class="sxs-lookup"><span data-stu-id="7e457-612">Updated USGovernmentActiveDirectoryEndpoint to https://login.microsoftonline.us/</span></span>
    - <span data-ttu-id="7e457-613">如需更多關於 Azure Government 端點對應的資訊，請參閱以下文章： https://docs.microsoft.com/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span><span class="sxs-lookup"><span data-stu-id="7e457-613">For more information about the Azure Government endpoint mappings, please see the following: https://docs.microsoft.com/azure/azure-government/documentation-government-developer-guide#endpoint-mapping</span></span>
    - <span data-ttu-id="7e457-614">新增 Cmdlet 的 -AsJob 支援，讓選取的 Cmdlet 可在背景中執行並傳回作業以追蹤和控制進度</span><span class="sxs-lookup"><span data-stu-id="7e457-614">Added -AsJob support for cmdlets, enabling selected cmdlets to execute in the background and return a job to track and control progress</span></span>
    - <span data-ttu-id="7e457-615">將 -AsJob 參數新增至 Get-AzureRmSubscription Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-615">Added -AsJob parameter to Get-AzureRmSubscription cmdlet</span></span>
* <span data-ttu-id="7e457-616">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7e457-616">RecoveryServices.Backup</span></span>
  - <span data-ttu-id="7e457-617">修正錯誤：Get-AzureRmRecoveryServicesBackupItem 應針對容器名稱的篩選，執行不區分大小寫的比較。</span><span class="sxs-lookup"><span data-stu-id="7e457-617">Fixed bug - Get-AzureRmRecoveryServicesBackupItem should do case insensitive comparison for container name filter.</span></span>
  - <span data-ttu-id="7e457-618">修正錯誤：AzureVmItem 現在有屬性可顯示最後一次發生備份作業的時間 (LastBackupTime)。</span><span class="sxs-lookup"><span data-stu-id="7e457-618">Fixed bug - AzureVmItem now has a property that shows the last time a backup operation has happened - LastBackupTime.</span></span>
* <span data-ttu-id="7e457-619">資源</span><span class="sxs-lookup"><span data-stu-id="7e457-619">Resources</span></span>
  - <span data-ttu-id="7e457-620">修正問題：Get-AzureRMRoleAssignment 產生的指派結果沒有自訂角色的角色定義名稱</span><span class="sxs-lookup"><span data-stu-id="7e457-620">Fixed issue where Get-AzureRMRoleAssignment would result in a assignments without roledefiniton name for custom roles</span></span>
    - <span data-ttu-id="7e457-621">使用者現在使用 Get-AzureRMRoleAssignment 產生的指派，會具有任何角色類型的角色定義名稱</span><span class="sxs-lookup"><span data-stu-id="7e457-621">Users can now use Get-AzureRMRoleAssignment with assignments having roledefinition names irrespective of the type of role</span></span>
  - <span data-ttu-id="7e457-622">修正問題：當可指派的範圍內有新範圍時，Set-AzureRMRoleRoleDefinition 會用來擲回找不到 RD 的錯誤</span><span class="sxs-lookup"><span data-stu-id="7e457-622">Fixed issue where Set-AzureRMRoleRoleDefinition used to throw RD not found error when there was a new scope in assignablescopes</span></span>
    - <span data-ttu-id="7e457-623">使用者現在能在可指派的範圍內有新範圍時，使用 Set-AzureRMRoleRoleDefinition，且不受限於範圍的位置</span><span class="sxs-lookup"><span data-stu-id="7e457-623">Users can now use Set-AzureRMRoleRoleDefinition with assignable scopes including new scopes irrespective of the position of the scope</span></span>
  - <span data-ttu-id="7e457-624">允許範圍以 "/" 結尾</span><span class="sxs-lookup"><span data-stu-id="7e457-624">Allow scopes to end with "/"</span></span>
    - <span data-ttu-id="7e457-625">使用者現在可以使用範圍結尾為 "/" 的 RoleDefinition 和 RoleAssignment Commandlet (與 API 和 CLI 一致)</span><span class="sxs-lookup"><span data-stu-id="7e457-625">Users can now use RoleDefinition and RoleAssignment commandlets with scopes ending with "/" ,consistent with API and CLI</span></span>
  - <span data-ttu-id="7e457-626">允許使用者使用委派旗標建立 RoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7e457-626">Allow users to create RoleAssignment using delegation flag</span></span>
    - <span data-ttu-id="7e457-627">使用者現在可以使用具有新增委派旗標選項的 New-AzureRMRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7e457-627">Users can now use New-AzureRMRoleAssignment with an option of adding the delegation flag</span></span>
  - <span data-ttu-id="7e457-628">修正 RoleAssignment 以遵守範圍參數</span><span class="sxs-lookup"><span data-stu-id="7e457-628">Fix RoleAssignment get to respect the scope parameter</span></span>
  - <span data-ttu-id="7e457-629">在 New-AzureRmRoleAssignment Commandlet 中新增 ServicePrincipalName 的別名</span><span class="sxs-lookup"><span data-stu-id="7e457-629">Add an alias for ServicePrincipalName in the New-AzureRmRoleAssignment Commandlet</span></span>
    - <span data-ttu-id="7e457-630">使用者現在使用 New-AzureRmRoleAssignment Commandlet 時，可使用 ApplicationId 而不是 ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7e457-630">Users can now use the ApplicationId instead of the ServicePrincipalName when using the New-AzureRmRoleAssignment commandlet</span></span>
* <span data-ttu-id="7e457-631">SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e457-631">SiteRecovery</span></span>
  - <span data-ttu-id="7e457-632">針對此模組中的所有 Cmdlet 新增取代警告，為下一次的重大變更發行做好準備。</span><span class="sxs-lookup"><span data-stu-id="7e457-632">Add deprecation warnings for all cmdlets in this module in preparation for the next breaking change release.</span></span>
    - <span data-ttu-id="7e457-633">請參閱即將發行的重大變更指南，以了解如何從 AzureRM 移轉您的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7e457-633">Please see the upcoming breaking changes guide for more information on how to migrate your cmdlets from AzureRM.</span></span>
* <span data-ttu-id="7e457-634">Sql</span><span class="sxs-lookup"><span data-stu-id="7e457-634">Sql</span></span>
  - <span data-ttu-id="7e457-635">新增使用 Set-AzureRmSqlDatabase 重新命名資料庫的功能</span><span class="sxs-lookup"><span data-stu-id="7e457-635">Added ability to rename database using Set-AzureRmSqlDatabase</span></span>
  - <span data-ttu-id="7e457-636">已修正的問題 https://github.com/Azure/azure-powershell/issues/4974</span><span class="sxs-lookup"><span data-stu-id="7e457-636">Fixed issue https://github.com/Azure/azure-powershell/issues/4974</span></span>
    - <span data-ttu-id="7e457-637">對稽核 Cmdlet 提供無效的 AUDIT_CHANGED_GROUP 值不會再擲回錯誤，並且將在近期版本中移除。</span><span class="sxs-lookup"><span data-stu-id="7e457-637">Providing invalid AUDIT_CHANGED_GROUP value for auditing cmdlets no longer throws an error and will be removed in an upcoming release.</span></span>
  - <span data-ttu-id="7e457-638">已修正的問題 https://github.com/Azure/azure-powershell/issues/5046</span><span class="sxs-lookup"><span data-stu-id="7e457-638">Fixed issue https://github.com/Azure/azure-powershell/issues/5046</span></span>
    - <span data-ttu-id="7e457-639">稽核 Cmdlet 中的 AuditAction 參數不再遭到忽略</span><span class="sxs-lookup"><span data-stu-id="7e457-639">AuditAction parameter in auditing cmdlets is no longer being ignored</span></span>
  - <span data-ttu-id="7e457-640">修正在稽核 Cmdlet 中提供 'Secondary' StorageKeyType 時的問題</span><span class="sxs-lookup"><span data-stu-id="7e457-640">Fixed an issue in Auditing cmdlets when 'Secondary' StorageKeyType is provided</span></span>
    - <span data-ttu-id="7e457-641">在設定 Blob 稽核時，針對 StorageKeyType 參數提供 'Secondary' 值時，系統使用的不是次要金鑰，而是主要儲存體帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="7e457-641">When setting blob auditing, the primary storage account key was used instead of the secondary key when providing 'Secondary' value for StorageKeyType parameter.</span></span>
  - <span data-ttu-id="7e457-642">變更 Set-AzureRmSqlServerTransparentDataEncryptionProtector 中的確認訊息文字</span><span class="sxs-lookup"><span data-stu-id="7e457-642">Changing the wording for confirmation message from Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>
* <span data-ttu-id="7e457-643">Azure (RDFE)</span><span class="sxs-lookup"><span data-stu-id="7e457-643">Azure (RDFE)</span></span>
    - <span data-ttu-id="7e457-644">移除所有 RemoteApp Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-644">Removed all RemoteApp Cmdles</span></span>
* <span data-ttu-id="7e457-645">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-645">Azure.Storage</span></span>
    - <span data-ttu-id="7e457-646">升級至 Azure 儲存體用戶端程式庫 8.6.0 及 Azure 儲存體資料移動程式庫 0.6.5</span><span class="sxs-lookup"><span data-stu-id="7e457-646">Upgrade to Azure Storage Client Library 8.6.0 and Azure Storage DataMovement Library 0.6.5</span></span>

## <a name="20171110-version-501"></a><span data-ttu-id="7e457-647">2017.11.10 版本 5.0.1</span><span class="sxs-lookup"><span data-stu-id="7e457-647">2017.11.10 Version 5.0.1</span></span>
* <span data-ttu-id="7e457-648">固定組件載入問題造成在下列模組中執行 Cmdlet 時失敗：</span><span class="sxs-lookup"><span data-stu-id="7e457-648">Fixed assembly loading issue that caused some cmdlets to fail when executing in the following modules:</span></span>
  - <span data-ttu-id="7e457-649">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e457-649">AzureRM.ApiManagement</span></span>
  - <span data-ttu-id="7e457-650">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="7e457-650">AzureRM.Backup</span></span>
  - <span data-ttu-id="7e457-651">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="7e457-651">AzureRM.Batch</span></span>
  - <span data-ttu-id="7e457-652">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="7e457-652">AzureRM.Compute</span></span>
  - <span data-ttu-id="7e457-653">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="7e457-653">AzureRM.DataFactories</span></span>
  - <span data-ttu-id="7e457-654">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7e457-654">AzureRM.HDInsight</span></span>
  - <span data-ttu-id="7e457-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7e457-655">AzureRM.KeyVault</span></span>
  - <span data-ttu-id="7e457-656">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7e457-656">AzureRM.RecoveryServices</span></span>
  - <span data-ttu-id="7e457-657">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7e457-657">AzureRM.RecoveryServices.Backup</span></span>
  - <span data-ttu-id="7e457-658">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e457-658">AzureRM.RecoveryServices.SiteRecovery</span></span>
  - <span data-ttu-id="7e457-659">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7e457-659">AzureRM.RedisCache</span></span>
  - <span data-ttu-id="7e457-660">AzureRM.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e457-660">AzureRM.SiteRecovery</span></span>
  - <span data-ttu-id="7e457-661">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="7e457-661">AzureRM.Sql</span></span>
  - <span data-ttu-id="7e457-662">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-662">AzureRM.Storage</span></span>
  - <span data-ttu-id="7e457-663">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e457-663">AzureRM.StreamAnalytics</span></span>

## <a name="2017118---version-500"></a><span data-ttu-id="7e457-664">2017.11.8 - 版本 5.0.0</span><span class="sxs-lookup"><span data-stu-id="7e457-664">2017.11.8 - Version 5.0.0</span></span>
* <span data-ttu-id="7e457-665">注意：這是重大變更版本。</span><span class="sxs-lookup"><span data-stu-id="7e457-665">NOTE: This is a breaking change release.</span></span> <span data-ttu-id="7e457-666">有關導入的重大變更完整清單，請參閱移轉指南 (https://aka.ms/azps-migration-guide) 。</span><span class="sxs-lookup"><span data-stu-id="7e457-666">Please see the migration guide (https://aka.ms/azps-migration-guide) for a full list of introduced breaking changes.</span></span>
* <span data-ttu-id="7e457-667">AzureRM 中所有的 Cmdlet 現在都支援線上說明</span><span class="sxs-lookup"><span data-stu-id="7e457-667">All cmdlets in AzureRM now support online help</span></span>
  - <span data-ttu-id="7e457-668">執行 Get-Help 搭配 -Online 參數，以在您的預設網際網路瀏覽器中開啟線上說明</span><span class="sxs-lookup"><span data-stu-id="7e457-668">Run Get-Help with the -Online parameter to open the online help in your default Internet browser</span></span>
* <span data-ttu-id="7e457-669">AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7e457-669">AnalysisServices</span></span>
  * <span data-ttu-id="7e457-670">固定的 Synchronize-AzureAsInstance 命令搭配使用新 AsAzure REST API 以進行同步處理</span><span class="sxs-lookup"><span data-stu-id="7e457-670">Fixed Synchronize-AzureAsInstance command to work with new AsAzure REST API for sync</span></span>
* <span data-ttu-id="7e457-671">ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7e457-671">ApiManagement</span></span>
  * <span data-ttu-id="7e457-672">有關 ApiManagement 在這一版所做的重大變更，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="7e457-672">Please see the migration guide for breaking changes made to ApiManagement this release</span></span>
  * <span data-ttu-id="7e457-673">已更新 Cmdlet Get-AzureRmApiManagementUser 以修正問題 https://github.com/Azure/azure-powershell/issues/4510</span><span class="sxs-lookup"><span data-stu-id="7e457-673">Updated Cmdlet Get-AzureRmApiManagementUser to fix issue https://github.com/Azure/azure-powershell/issues/4510</span></span>
  * <span data-ttu-id="7e457-674">已更新 Cmdlet New-AzureRmApiManagementApi 以建立具備 Empty Path 的 API https://github.com/Azure/azure-powershell/issues/4069</span><span class="sxs-lookup"><span data-stu-id="7e457-674">Updated Cmdlet New-AzureRmApiManagementApi to create Api with Empty Path https://github.com/Azure/azure-powershell/issues/4069</span></span>
* <span data-ttu-id="7e457-675">ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7e457-675">ApplicationInsights</span></span>
  * <span data-ttu-id="7e457-676">新增命令以取得/建立/移除應用程式深入解析資源</span><span class="sxs-lookup"><span data-stu-id="7e457-676">Add commands to get/create/remove applicaiton insights resource</span></span>
    - <span data-ttu-id="7e457-677">Get-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7e457-677">Get-AzureRmApplicationInsights</span></span>
    - <span data-ttu-id="7e457-678">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7e457-678">New-AzureRmApplicationInsights</span></span>
    - <span data-ttu-id="7e457-679">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7e457-679">Remove-AzureRmApplicationInsights</span></span>
  * <span data-ttu-id="7e457-680">新增命令以取得/更新價格/應用程式深入解析資源的每日上限</span><span class="sxs-lookup"><span data-stu-id="7e457-680">Add commands to get/update pricing/daily cap of applicaiton insights resource</span></span>
    - <span data-ttu-id="7e457-681">Get-AzureRmApplicationInsights -IncludeDailyCap</span><span class="sxs-lookup"><span data-stu-id="7e457-681">Get-AzureRmApplicationInsights -IncludeDailyCap</span></span>
    - <span data-ttu-id="7e457-682">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="7e457-682">Set-AzureRmApplicationInsightsPricingPlan</span></span>
    - <span data-ttu-id="7e457-683">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="7e457-683">Set-AzureRmApplicationInsightsDailyCap</span></span>
  * <span data-ttu-id="7e457-684">新增命令以取得/建立/更新/移除應用程式深入解析資源的連續匯出</span><span class="sxs-lookup"><span data-stu-id="7e457-684">Add commands to get/create/update/remove continuous export of applicaiton insights resource</span></span>
    - <span data-ttu-id="7e457-685">Get-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7e457-685">Get-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="7e457-686">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7e457-686">Set-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="7e457-687">New-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7e457-687">New-AzureRmApplicationInsightsContinuousExport</span></span>
    - <span data-ttu-id="7e457-688">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7e457-688">Remove-AzureRmApplicationInsightsContinuousExport</span></span>
  * <span data-ttu-id="7e457-689">新增命令以取得/建立/移除應用程式深入解析資源的 API 金鑰</span><span class="sxs-lookup"><span data-stu-id="7e457-689">Add commands to get/create/remove api keys of applicaiton insights resoruce</span></span>
    - <span data-ttu-id="7e457-690">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="7e457-690">Get-AzureRmApplicationInsightsApiKey</span></span>
    - <span data-ttu-id="7e457-691">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="7e457-691">New-AzureRmApplicationInsightsApiKey</span></span>
    - <span data-ttu-id="7e457-692">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="7e457-692">Remove-AzureRmApplicationInsightsApiKey</span></span>
* <span data-ttu-id="7e457-693">AzureBatch</span><span class="sxs-lookup"><span data-stu-id="7e457-693">AzureBatch</span></span>
  * <span data-ttu-id="7e457-694">將新參數新增至 `New-AzureRmBatchAccount`。</span><span class="sxs-lookup"><span data-stu-id="7e457-694">Added new parameters to `New-AzureRmBatchAccount`.</span></span>
    - <span data-ttu-id="7e457-695">`PoolAllocationMode`:在 Batch 帳戶中建立集區所使用的配置模式。</span><span class="sxs-lookup"><span data-stu-id="7e457-695">`PoolAllocationMode`: The allocation mode to use for creating pools in the Batch account.</span></span> <span data-ttu-id="7e457-696">若要在使用者的訂用帳戶中建立配置集區節點的 Batch 帳戶，請將此設為 `UserSubscription`。</span><span class="sxs-lookup"><span data-stu-id="7e457-696">To create a Batch account which allocates pool nodes in the user's subscription, set this to `UserSubscription`.</span></span>
    - <span data-ttu-id="7e457-697">`KeyVaultId`:與 Batch 帳戶相關的 Azure Key Vault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7e457-697">`KeyVaultId`: The resource ID of the Azure key vault associated with the Batch account.</span></span>
    - <span data-ttu-id="7e457-698">`KeyVaultUrl`:與 Batch 帳戶相關的 Azure Key Vault URL。</span><span class="sxs-lookup"><span data-stu-id="7e457-698">`KeyVaultUrl`: The URL of the Azure key vault associated with the Batch account.</span></span>
  * <span data-ttu-id="7e457-699">將參數更新為 `New-AzureBatchTask`。</span><span class="sxs-lookup"><span data-stu-id="7e457-699">Updated parameters to `New-AzureBatchTask`.</span></span>
    - <span data-ttu-id="7e457-700">移除 `RunElevated` 參數。</span><span class="sxs-lookup"><span data-stu-id="7e457-700">Removed the `RunElevated` switch.</span></span> <span data-ttu-id="7e457-701">已新增 `UserIdentity` 參數來取代 `RunElevated`，且對等的行為可藉由建構 `PSUserIdentity` 來達成，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7e457-701">The `UserIdentity` parameter has been added to replace `RunElevated`, and the equivalent behavior can be achieved by constructing a `PSUserIdentity` as shown below:</span></span>
      - <span data-ttu-id="7e457-702">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span><span class="sxs-lookup"><span data-stu-id="7e457-702">$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")</span></span>
      - <span data-ttu-id="7e457-703">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span><span class="sxs-lookup"><span data-stu-id="7e457-703">$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser</span></span>
    - <span data-ttu-id="7e457-704">新增 `AuthenticationTokenSettings` 參數。</span><span class="sxs-lookup"><span data-stu-id="7e457-704">Added the `AuthenticationTokenSettings` parameter.</span></span> <span data-ttu-id="7e457-705">這個參數可讓您要求 Batch 服務在執行時向工作提供驗證權杖，而不必先將 Batch 帳戶金鑰傳遞至工作，才能對 Batch 服務發出要求。</span><span class="sxs-lookup"><span data-stu-id="7e457-705">This parameter allows you to request the Batch service provide an authentication token to the task when it runs, avoiding the need to pass Batch account keys to the task in order to issue requests to the Batch service.</span></span>
    - <span data-ttu-id="7e457-706">新增 `ContainerSettings` 參數。</span><span class="sxs-lookup"><span data-stu-id="7e457-706">Added the `ContainerSettings` parameter.</span></span>
      - <span data-ttu-id="7e457-707">這個參數可讓您要求 Batch 服務在容器內執行工作。</span><span class="sxs-lookup"><span data-stu-id="7e457-707">This parameter allows you to request the Batch service run the task inside a container.</span></span>
    - <span data-ttu-id="7e457-708">新增 `OutputFiles` 參數。</span><span class="sxs-lookup"><span data-stu-id="7e457-708">Added the `OutputFiles` parameter.</span></span>
      - <span data-ttu-id="7e457-709">這個參數可讓您設定在工作完成之後將檔案上傳至 Azure 儲存體。</span><span class="sxs-lookup"><span data-stu-id="7e457-709">This parameter allows you to configure the task to upload files to Azure Storage after it has finished.</span></span>
  * <span data-ttu-id="7e457-710">將參數更新為 `New-AzureBatchPool`。</span><span class="sxs-lookup"><span data-stu-id="7e457-710">Updated parameters to `New-AzureBatchPool`.</span></span>
    - <span data-ttu-id="7e457-711">新增 `UserAccounts` 參數。</span><span class="sxs-lookup"><span data-stu-id="7e457-711">Added the `UserAccounts` parameter.</span></span>
      - <span data-ttu-id="7e457-712">這個參數可定義集區中每個節點上所建立的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="7e457-712">This parameter defines user accounts created on each node in the pool.</span></span>
    - <span data-ttu-id="7e457-713">新增 `TargetLowPriorityComputeNodes` 並將 `TargetDedicated` 重新命名為 `TargetDedicatedComputeNodes`。</span><span class="sxs-lookup"><span data-stu-id="7e457-713">Added `TargetLowPriorityComputeNodes` and renamed `TargetDedicated` to `TargetDedicatedComputeNodes`.</span></span>
      - <span data-ttu-id="7e457-714">針對 `TargetDedicatedComputeNodes` 參數已建立 `TargetDedicated` 別名。</span><span class="sxs-lookup"><span data-stu-id="7e457-714">A `TargetDedicated` alias was created for the `TargetDedicatedComputeNodes` parameter.</span></span>
    - <span data-ttu-id="7e457-715">新增 `NetworkConfiguration` 參數。</span><span class="sxs-lookup"><span data-stu-id="7e457-715">Added the `NetworkConfiguration` parameter.</span></span>
      - <span data-ttu-id="7e457-716">這個參數可讓您設定集區的網路設定。</span><span class="sxs-lookup"><span data-stu-id="7e457-716">This parameter allows you to configure the pools network settings.</span></span>
  * <span data-ttu-id="7e457-717">將參數更新為 `New-AzureBatchCertificate`。</span><span class="sxs-lookup"><span data-stu-id="7e457-717">Updated parameters to `New-AzureBatchCertificate`.</span></span>
    - <span data-ttu-id="7e457-718">`Password` 參數現在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="7e457-718">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="7e457-719">將參數更新為 `New-AzureBatchComputeNodeUser`。</span><span class="sxs-lookup"><span data-stu-id="7e457-719">Updated parameters to `New-AzureBatchComputeNodeUser`.</span></span>
    - <span data-ttu-id="7e457-720">`Password` 參數現在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="7e457-720">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="7e457-721">將參數更新為 `Set-AzureBatchComputeNodeUser`。</span><span class="sxs-lookup"><span data-stu-id="7e457-721">Updated parameters to `Set-AzureBatchComputeNodeUser`.</span></span>
    - <span data-ttu-id="7e457-722">`Password` 參數現在是 `SecureString`。</span><span class="sxs-lookup"><span data-stu-id="7e457-722">The `Password` parameter is now a `SecureString`.</span></span>
  * <span data-ttu-id="7e457-723">在 `Get-AzureBatchNodeFile`、`Get-AzureBatchNodeFileContent` 和 `Remove-AzureBatchNodeFile` 上將 `Name` 參數重新命名為 `Path`。</span><span class="sxs-lookup"><span data-stu-id="7e457-723">Renamed the `Name` parameter to `Path` on `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent`, and `Remove-AzureBatchNodeFile`.</span></span>
    - <span data-ttu-id="7e457-724">針對 `Path` 參數已建立 `Name` 別名。</span><span class="sxs-lookup"><span data-stu-id="7e457-724">A `Name` alias was created for the `Path` parameter.</span></span>
  * <span data-ttu-id="7e457-725">物件的變更</span><span class="sxs-lookup"><span data-stu-id="7e457-725">Changes to objects</span></span>
    - <span data-ttu-id="7e457-726">請參閱 Batch 變更記錄取得完整清單</span><span class="sxs-lookup"><span data-stu-id="7e457-726">Please see the Batch change log for the full list</span></span>
  * <span data-ttu-id="7e457-727">新增 Azure Active Directory 型驗證支援。</span><span class="sxs-lookup"><span data-stu-id="7e457-727">Added support for Azure Active Directory based authentication.</span></span>
    - <span data-ttu-id="7e457-728">若要使用 Azure Active Directory 驗證，請使用 `Get-AzureRmBatchAccount` Cmdlet 擷取 `BatchAccountContext` 物件，並將此 `BatchAccountContext` 提供至 Batch 服務 Cmdlet 的 `-BatchContext` 參數。</span><span class="sxs-lookup"><span data-stu-id="7e457-728">To use Azure Active Directory authentication, retrieve a `BatchAccountContext` object using the `Get-AzureRmBatchAccount` cmdlet, and supply this `BatchAccountContext` to the `-BatchContext` parameter of a Batch service cmdlet.</span></span> <span data-ttu-id="7e457-729">對於具有 `PoolAllocationMode = UserSubscription` 的帳戶，Azure Active Directory 驗證為必要。</span><span class="sxs-lookup"><span data-stu-id="7e457-729">Azure Active Directory authentication is mandatory for accounts with `PoolAllocationMode = UserSubscription`.</span></span>
    - <span data-ttu-id="7e457-730">對於現有帳戶或以 `PoolAllocationMode = BatchService` 建立的新帳戶，您可以藉由使用 `Get-AzureRmBatchAccoutKeys` Cmdlet 擷取 `BatchAccountContext` 物件，繼續使用共用金鑰驗證。</span><span class="sxs-lookup"><span data-stu-id="7e457-730">For existing accounts or for new accounts created with `PoolAllocationMode = BatchService`, you may continue to use shared key authentication by retrieving a `BatchAccountContext` object using the `Get-AzureRmBatchAccoutKeys` cmdlet.</span></span>
* <span data-ttu-id="7e457-731">計算</span><span class="sxs-lookup"><span data-stu-id="7e457-731">Compute</span></span>
  * <span data-ttu-id="7e457-732">Azure 磁碟加密延伸模組命令</span><span class="sxs-lookup"><span data-stu-id="7e457-732">Azure Disk Encryption Extension Commands</span></span>
    - <span data-ttu-id="7e457-733">'Set-AzureRmVmDiskEncryptionExtension' 的新參數：'-EncryptFormatAll' 加密格式資料磁碟</span><span class="sxs-lookup"><span data-stu-id="7e457-733">New Parameter for 'Set-AzureRmVmDiskEncryptionExtension': '-EncryptFormatAll' encrypt formats data disks</span></span>
    - <span data-ttu-id="7e457-734">'Set-AzureRmVmDiskEncryptionExtension' 的新參數：'-ExtensionPublisherName' 和 '-ExtensionType' 允許切換至延伸模組的其他版本</span><span class="sxs-lookup"><span data-stu-id="7e457-734">New Parameters for 'Set-AzureRmVmDiskEncryptionExtension': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
    - <span data-ttu-id="7e457-735">'Disable-AzureRmVmDiskEncryption' 的新參數：'-ExtensionPublisherName' 和 '-ExtensionType' 允許切換至延伸模組的其他版本</span><span class="sxs-lookup"><span data-stu-id="7e457-735">New Parameters for 'Disable-AzureRmVmDiskEncryption': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
    - <span data-ttu-id="7e457-736">'Get-AzureRmVmDiskEncryptionStatus' 的新參數：'-ExtensionPublisherName' 和 '-ExtensionType' 允許切換至延伸模組的其他版本</span><span class="sxs-lookup"><span data-stu-id="7e457-736">New Parameters for 'Get-AzureRmVmDiskEncryptionStatus': '-ExtensionPublisherName' and '-ExtensionType' allow switching to other versions of the extension</span></span>
* <span data-ttu-id="7e457-737">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7e457-737">DataLakeAnalytics</span></span>
  * <span data-ttu-id="7e457-738">有關 DataLakeAnalytics 在這一版所做的重大變更，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="7e457-738">Please see the migration guide for breaking changes made to DataLakeAnalytics this release</span></span>
  * <span data-ttu-id="7e457-739">變更 Get-AzureRmDataLakeAnalyticsAccount 兩種 OutputTypes 的其中一種</span><span class="sxs-lookup"><span data-stu-id="7e457-739">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsAccount</span></span>
    - <span data-ttu-id="7e457-740">清單\<DataLakeAnalyticsAccount> 至清單\<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="7e457-740">List\<DataLakeAnalyticsAccount> to List\<PSDataLakeAnalyticsAccountBasic></span></span>
    - <span data-ttu-id="7e457-741">PSDataLakeAnalyticsAccountBasic 的屬性是 DataLakeAnalyticsAccount 屬性的 strict 子集</span><span class="sxs-lookup"><span data-stu-id="7e457-741">The properties of PSDataLakeAnalyticsAccountBasic is a strict subset of the properties of DataLakeAnalyticsAccount</span></span>
    - <span data-ttu-id="7e457-742">服務不會傳回 DataLakeAnalyticsAccount 中的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="7e457-742">The additional properties that are in DataLakeAnalyticsAccount are not returned by the service.</span></span>  <span data-ttu-id="7e457-743">因此，這項變更是為了準確反映此情況。</span><span class="sxs-lookup"><span data-stu-id="7e457-743">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="7e457-744">這些額外屬性仍然在 PSDataLakeAnalyticsAccountBasic 中，但被標記為 [已淘汰]。</span><span class="sxs-lookup"><span data-stu-id="7e457-744">These additional properties are still in PSDataLakeAnalyticsAccountBasic, but they are tagged as Obsolete.</span></span>
  * <span data-ttu-id="7e457-745">變更 Get-AzureRmDataLakeAnalyticsJob 兩種 OutputTypes 的其中一種</span><span class="sxs-lookup"><span data-stu-id="7e457-745">Changed one of the two OutputTypes of Get-AzureRmDataLakeAnalyticsJob</span></span>
    - <span data-ttu-id="7e457-746">清單\<JobInformation> 至清單\<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="7e457-746">List\<JobInformation> to List\<PSJobInformationBasic></span></span>
    - <span data-ttu-id="7e457-747">PSJobInformationBasic 的屬性是 JobInformation 屬性的 strict 子集</span><span class="sxs-lookup"><span data-stu-id="7e457-747">The properties of PSJobInformationBasic is a strict subset of the properties of JobInformation</span></span>
    - <span data-ttu-id="7e457-748">服務不會傳回 JobInformation 中的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="7e457-748">The additional properties that are in JobInformation are not returned by the service.</span></span>  <span data-ttu-id="7e457-749">因此，這項變更是為了準確反映此情況。</span><span class="sxs-lookup"><span data-stu-id="7e457-749">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="7e457-750">這些額外屬性仍然在 PSJobInformationBasic 中，但被標記為 [已淘汰]。</span><span class="sxs-lookup"><span data-stu-id="7e457-750">These additional properties are still in PSJobInformationBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="7e457-751">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7e457-751">DataLakeStore</span></span>
  * <span data-ttu-id="7e457-752">有關 DataLakeStore 在這一版所做的重大變更，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="7e457-752">Please see the migration guide for breaking changes made to DataLakeStore this release</span></span>
  * <span data-ttu-id="7e457-753">變更 Get-AzureRmDataLakeStoreAccount 兩種 OutputTypes 的其中一種</span><span class="sxs-lookup"><span data-stu-id="7e457-753">Changed one of the two OutputTypes of Get-AzureRmDataLakeStoreAccount</span></span>
    - <span data-ttu-id="7e457-754">清單\<PSDataLakeStoreAccount> 至清單\<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="7e457-754">List\<PSDataLakeStoreAccount> to List\<PSDataLakeStoreAccountBasic></span></span>
    - <span data-ttu-id="7e457-755">PSDataLakeStoreAccountBasic 的屬性是 PSDataLakeStoreAccount 屬性的 strict 子集</span><span class="sxs-lookup"><span data-stu-id="7e457-755">The properties of PSDataLakeStoreAccountBasic is a strict subset of the properties of PSDataLakeStoreAccount</span></span>
    - <span data-ttu-id="7e457-756">服務不會傳回 PSDataLakeStoreAccount 中的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="7e457-756">The additional properties that are in PSDataLakeStoreAccount are not returned by the service.</span></span>  <span data-ttu-id="7e457-757">因此，這項變更是為了準確反映此情況。</span><span class="sxs-lookup"><span data-stu-id="7e457-757">Therefore, this change is to reflect this accurately.</span></span> <span data-ttu-id="7e457-758">這些額外屬性仍然在 PSDataLakeStoreAccountBasic 中，但被標記為 [已淘汰]。</span><span class="sxs-lookup"><span data-stu-id="7e457-758">These additional properties are still in PSDataLakeStoreAccountBasic, but they are tagged as Obsolete.</span></span>
* <span data-ttu-id="7e457-759">Dns</span><span class="sxs-lookup"><span data-stu-id="7e457-759">Dns</span></span>
  * <span data-ttu-id="7e457-760">Azure DNS 中 CAA 記錄型別的支援</span><span class="sxs-lookup"><span data-stu-id="7e457-760">Support for CAA record types in Azure DNS</span></span>
    - <span data-ttu-id="7e457-761">支援 CAA 記錄型別上的所有作業</span><span class="sxs-lookup"><span data-stu-id="7e457-761">Supports all operations on CAA record type</span></span>
* <span data-ttu-id="7e457-762">EventHub</span><span class="sxs-lookup"><span data-stu-id="7e457-762">EventHub</span></span>
  * <span data-ttu-id="7e457-763">有關 EventHub 在這一版所做的重大變更，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="7e457-763">Please see the migration guide for breaking changes made to EventHub this release</span></span>
* <span data-ttu-id="7e457-764">深入解析</span><span class="sxs-lookup"><span data-stu-id="7e457-764">Insights</span></span>
  * <span data-ttu-id="7e457-765">有關深入解析在這一版所做的重大變更，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="7e457-765">Please see the migration guide for breaking changes made to Insights this release</span></span>
* <span data-ttu-id="7e457-766">網路</span><span class="sxs-lookup"><span data-stu-id="7e457-766">Network</span></span>
  * <span data-ttu-id="7e457-767">有關網路在這一版所做的重大變更，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="7e457-767">Please see the migration guide for breaking changes made to Network this release</span></span>
  * <span data-ttu-id="7e457-768">新增 Cmdlet 以針對指定的 Azure 區域列出可用的網際網路服務提供者</span><span class="sxs-lookup"><span data-stu-id="7e457-768">Added cmdlet to list available internet service providers for a specified Azure region</span></span>
    - <span data-ttu-id="7e457-769">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7e457-769">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>
  * <span data-ttu-id="7e457-770">新增 Cmdlet 以取得從指定位置到 Azure 區域的網際網路服務提供者相對延遲分數</span><span class="sxs-lookup"><span data-stu-id="7e457-770">Added cmdlet to get the relative latency score for internet service providers from a specified location to Azure regions</span></span>
    - <span data-ttu-id="7e457-771">Get-AzureRmNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7e457-771">Get-AzureRmNetworkWatcherReachabilityReport</span></span>
* <span data-ttu-id="7e457-772">設定檔</span><span class="sxs-lookup"><span data-stu-id="7e457-772">Profile</span></span>
  - <span data-ttu-id="7e457-773">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="7e457-773">Set-AzureRmDefault</span></span>
    - <span data-ttu-id="7e457-774">使用這個 Cmdlet 設定預設的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7e457-774">Use this cmdlet to set a default resource group.</span></span>  <span data-ttu-id="7e457-775">對於某些 Cmdlet，這會讓 -ResourceGroup 參數成為選用，且在未指定資源群組時將使用預設值</span><span class="sxs-lookup"><span data-stu-id="7e457-775">This will make the -ResourceGroup parameter optional for some cmdlets, and will use the default when a resource group is not specified</span></span>
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - <span data-ttu-id="7e457-776">如果指定的資源群組存在於訂用帳戶中，則此資源群組將會設為預設值。</span><span class="sxs-lookup"><span data-stu-id="7e457-776">If resource group specified exists in the subscription, this resource group will be set to default.</span></span>  <span data-ttu-id="7e457-777">否則，將會建立該資源群組，並將其設為預設值。</span><span class="sxs-lookup"><span data-stu-id="7e457-777">Otherwise, the resource group will be created and then set to default.</span></span>
  - <span data-ttu-id="7e457-778">Get-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="7e457-778">Get-AzureRmDefault</span></span>
    - <span data-ttu-id="7e457-779">使用這個 Cmdlet 取得目前預設的資源群組 (和未來其他的預設)。</span><span class="sxs-lookup"><span data-stu-id="7e457-779">Use this cmdlet to get the current default resource group (and other defaults in the future).</span></span>
    - ```Get-AzureRmDefault -ResourceGroup```
  - <span data-ttu-id="7e457-780">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="7e457-780">Clear-AzureRmDefault</span></span>
    - <span data-ttu-id="7e457-781">使用這個 Cmdlet 移除目前預設的資源群組</span><span class="sxs-lookup"><span data-stu-id="7e457-781">Use this cmdlet to remove the current default resource group</span></span>
    - ```Clear-AzureRmDefault -ResourceGroup```
  - <span data-ttu-id="7e457-782">Add-AzureRmEnvironment 和 Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e457-782">Add-AzureRmEnvironment and Set-AzureRmEnvironment</span></span>
    - <span data-ttu-id="7e457-783">新增 BatchAudience 參數，可讓您指定在取得 Batch 服務驗證權杖時所要使用的 Azure Batch Active Directory 對象。</span><span class="sxs-lookup"><span data-stu-id="7e457-783">Add the BatchAudience parameter, which allows you to specify the Azure Batch Active Directory audience to use when acquiring authentication tokens for the Batch service.</span></span>
* <span data-ttu-id="7e457-784">RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7e457-784">RecoveryServices.Backup</span></span>
  * <span data-ttu-id="7e457-785">新增 Cmdlet 以執行立即檔案復原。</span><span class="sxs-lookup"><span data-stu-id="7e457-785">Added cmdlets to perform instant file recovery.</span></span>
    - <span data-ttu-id="7e457-786">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="7e457-786">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>
    - <span data-ttu-id="7e457-787">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="7e457-787">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>
  * <span data-ttu-id="7e457-788">將 RecoveryServices.Backup SDK 更新至最新版本</span><span class="sxs-lookup"><span data-stu-id="7e457-788">Updated RecoveryServices.Backup SDK version to the latest</span></span>
  * <span data-ttu-id="7e457-789">更新 Azure VM 工作負載的測試，如此一來測試回合所需的所有設定便由測試本身完成。</span><span class="sxs-lookup"><span data-stu-id="7e457-789">Updated tests for the Azure VM workload so that, all setups needed for test runs are done by the tests themselves.</span></span>
  * <span data-ttu-id="7e457-790">修正 https://github.com/Azure/azure-powershell/issues/3164</span><span class="sxs-lookup"><span data-stu-id="7e457-790">Fixes https://github.com/Azure/azure-powershell/issues/3164</span></span>
* <span data-ttu-id="7e457-791">RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7e457-791">RecoveryServices.SiteRecovery</span></span>
  * <span data-ttu-id="7e457-792">ASR VMware 到 Azure Site Recovery 的變更 (Cmdlet 目前支援企業到企業、企業到 Azure、HyperV 到 Azure 的作業)</span><span class="sxs-lookup"><span data-stu-id="7e457-792">Changes for ASR VMware to Azure Site Recovery (cmdlets are currently supporting operations for Enterprise to Enterprise, Enterprise to Azure, HyperV to Azure)</span></span>
    - <span data-ttu-id="7e457-793">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7e457-793">New-AzureRmRecoveryServicesAsrPolicy</span></span>
    - <span data-ttu-id="7e457-794">New-AzureRmRecoveryServicesAsrProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7e457-794">New-AzureRmRecoveryServicesAsrProtectedItem</span></span>
    - <span data-ttu-id="7e457-795">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7e457-795">Update-AzureRmRecoveryServicesAsrPolicy</span></span>
    - <span data-ttu-id="7e457-796">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="7e457-796">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>
  * <span data-ttu-id="7e457-797">新增以 AAD 為基礎的保存庫支援</span><span class="sxs-lookup"><span data-stu-id="7e457-797">Added support to AAD-based vault</span></span>
  * <span data-ttu-id="7e457-798">新增 Cmdlet 以管理 VCenter 資源</span><span class="sxs-lookup"><span data-stu-id="7e457-798">Added cmdlets to manage VCenter resources</span></span>
    - <span data-ttu-id="7e457-799">Get-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="7e457-799">Get-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="7e457-800">New-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="7e457-800">New-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="7e457-801">Remove-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="7e457-801">Remove-AzureRmRecoveryServicesAsrVCenter</span></span>
    - <span data-ttu-id="7e457-802">Update-AzureRmRecoveryServicesAsrVCenter</span><span class="sxs-lookup"><span data-stu-id="7e457-802">Update-AzureRmRecoveryServicesAsrVCenter</span></span>
  * <span data-ttu-id="7e457-803">新增其他 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7e457-803">Added other cmdlets</span></span>
    - <span data-ttu-id="7e457-804">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="7e457-804">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>
    - <span data-ttu-id="7e457-805">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="7e457-805">Get-AzureRmRecoveryServicesAsrEvent</span></span>
    - <span data-ttu-id="7e457-806">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7e457-806">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
    - <span data-ttu-id="7e457-807">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="7e457-807">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>
    - <span data-ttu-id="7e457-808">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="7e457-808">Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob</span></span>
    - <span data-ttu-id="7e457-809">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="7e457-809">Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob</span></span>
    - <span data-ttu-id="7e457-810">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="7e457-810">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>
    - <span data-ttu-id="7e457-811">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="7e457-811">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>
* <span data-ttu-id="7e457-812">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7e457-812">ServiceBus</span></span>
  - <span data-ttu-id="7e457-813">有關 ServiceBus 在這一版所做的重大變更，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="7e457-813">Please see the migration guide for breaking changes made to ServiceBus this release</span></span>
* <span data-ttu-id="7e457-814">Sql</span><span class="sxs-lookup"><span data-stu-id="7e457-814">Sql</span></span>
  * <span data-ttu-id="7e457-815">新增對列出和取消資料庫上非同步 updateslo 作業的支援</span><span class="sxs-lookup"><span data-stu-id="7e457-815">Adding support for list and cancel the asynchronous updateslo operation on the database</span></span>
    - <span data-ttu-id="7e457-816">更新現有的 Cmdlet Get-AzureRmSqlDatabaseActivity 以傳回 DB updateslo 作業狀態。</span><span class="sxs-lookup"><span data-stu-id="7e457-816">update existing cmdlet Get-AzureRmSqlDatabaseActivity to return DB updateslo operation status.</span></span>
    - <span data-ttu-id="7e457-817">新增新的 Cmdlet Stop-AzureRmSqlDatabaseActivity 以取消資料庫上的非同步 updateslo 作業。</span><span class="sxs-lookup"><span data-stu-id="7e457-817">add new cmdlet Stop-AzureRmSqlDatabaseActivity for cancel the asynchronous updateslo operation on the database.</span></span>
  * <span data-ttu-id="7e457-818">新增對資料庫和彈性集區的區域備援支援</span><span class="sxs-lookup"><span data-stu-id="7e457-818">Adding support for Zone Redundancy for databases and elastic pools</span></span>
    - <span data-ttu-id="7e457-819">將 ZoneRedundant 切換參數新增至 New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e457-819">Adding ZoneRedundant switch parameter to New-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="7e457-820">將 ZoneRedundant 切換參數新增至 Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="7e457-820">Adding ZoneRedundant switch parameter to Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="7e457-821">將 ZoneRedundant 切換參數新增至 New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7e457-821">Adding ZoneRedundant switch parameter to New-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="7e457-822">將 ZoneRedundant 切換參數新增至 Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7e457-822">Adding ZoneRedundant switch parameter to Set-AzureRmSqlElasticPool</span></span>
  * <span data-ttu-id="7e457-823">新增對伺服器 DNS 別名的支援</span><span class="sxs-lookup"><span data-stu-id="7e457-823">Adding support for Server DNS Aliases</span></span>
    - <span data-ttu-id="7e457-824">新增 Get-AzureRmSqlServerDnsAlias Cmdlet，其可按照伺服器和別名名稱取得伺服器 dns 別名，或 Azure Sql Server 的伺服器 dns 別名清單。</span><span class="sxs-lookup"><span data-stu-id="7e457-824">Adding Get-AzureRmSqlServerDnsAlias cmdlet which gets server dns aliases by server and alias name or a list of server dns aliases for an azure Sql Server.</span></span>
    - <span data-ttu-id="7e457-825">新增 New-AzureRmSqlServerDnsAlias Cmdlet，其可建立指定的 Azure Sql 伺服器的新伺服器 dns 別名</span><span class="sxs-lookup"><span data-stu-id="7e457-825">Adding New-AzureRmSqlServerDnsAlias cmdlet which creates new server dns alias for a given Azure Sql server</span></span>
    - <span data-ttu-id="7e457-826">新增 Set-AzurermSqlServerDnsAlias Cmdlet，其可讓伺服器 dns 別名指向的 Azure Sql Server 進行更新</span><span class="sxs-lookup"><span data-stu-id="7e457-826">Adding Set-AzurermSqlServerDnsAlias cmlet which allows updating a Azure Sql Server to which server dns alias is pointing</span></span>
    - <span data-ttu-id="7e457-827">新增 Remove-AzureRmSqlServerDnsAlias Cmdlet，其可移除 Azure Sql 伺服器的伺服器 dns 別名</span><span class="sxs-lookup"><span data-stu-id="7e457-827">Adding Remove-AzureRmSqlServerDnsAlias cmdlet which removes a server dns alias for a Azure Sql Server</span></span>
* <span data-ttu-id="7e457-828">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7e457-828">Azure.Storage</span></span>
  * <span data-ttu-id="7e457-829">升級至 Azure 儲存體用戶端程式庫 8.5.0 及 Azure 儲存體資料移動程式庫 0.6.3</span><span class="sxs-lookup"><span data-stu-id="7e457-829">Upgrade to Azure Storage Client Library 8.5.0 and Azure Storage DataMovement Library 0.6.3</span></span>
  * <span data-ttu-id="7e457-830">新增檔案共用快照集支援功能</span><span class="sxs-lookup"><span data-stu-id="7e457-830">Add File Share Snapshot Support Feature</span></span>
    - <span data-ttu-id="7e457-831">將 'SnapshotTime' 參數新增至 Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e457-831">Add 'SnapshotTime' parameter to Get-AzureStorageShare</span></span>
    - <span data-ttu-id="7e457-832">將 'IncludeAllSnapshot' 參數新增至 Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e457-832">Add 'IncludeAllSnapshot' parameter to Remove-AzureStorageShare</span></span>
