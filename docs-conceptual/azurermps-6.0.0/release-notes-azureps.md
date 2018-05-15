---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="21ce8-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="21ce8-103">Release notes</span></span>

<span data-ttu-id="21ce8-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="21ce8-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="21ce8-105">6.0.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="21ce8-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="21ce8-106">一般</span><span class="sxs-lookup"><span data-stu-id="21ce8-106">General</span></span>
* <span data-ttu-id="21ce8-107">將模組的最小相依性設定為 PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="21ce8-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="21ce8-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="21ce8-108">Azure.Storage</span></span>
* <span data-ttu-id="21ce8-109">支援做為儲存體 Blob 容器名稱</span><span class="sxs-lookup"><span data-stu-id="21ce8-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="21ce8-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="21ce8-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="21ce8-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="21ce8-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="21ce8-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="21ce8-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="21ce8-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="21ce8-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="21ce8-114">修正此問題：某些儲存體 Cmdlet 失敗輸出未包含詳細的失敗資訊</span><span class="sxs-lookup"><span data-stu-id="21ce8-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="21ce8-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="21ce8-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="21ce8-116">推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-117">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="21ce8-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="21ce8-118">AzureRM.Automation</span></span>
* <span data-ttu-id="21ce8-119">從 Cmdlet 移除取代的 'Tags' 別名</span><span class="sxs-lookup"><span data-stu-id="21ce8-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="21ce8-120">'Set-AzureRmAutomationRunbook'</span><span class="sxs-lookup"><span data-stu-id="21ce8-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="21ce8-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="21ce8-121">AzureRM.Batch</span></span>
* <span data-ttu-id="21ce8-122">已更新 New-AzureBatchPool 文件以移除取代的範例</span><span class="sxs-lookup"><span data-stu-id="21ce8-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="21ce8-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="21ce8-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="21ce8-124">推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-125">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="21ce8-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="21ce8-126">AzureRM.Compute</span></span>
* <span data-ttu-id="21ce8-127">'New-AzureRmVm' 和 'New-AzureRmVmss' 支援參數的詳細資訊輸出</span><span class="sxs-lookup"><span data-stu-id="21ce8-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="21ce8-128">'New-AzureRmVm' 和 'New-AzureRmVmss' (簡單參數集) 支援將使用者定義和 (或) 系統定義的身分識別指派至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="21ce8-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="21ce8-129">VMSS 重新部署和執行維護功能</span><span class="sxs-lookup"><span data-stu-id="21ce8-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="21ce8-130">將新的切換參數 -Redeploy 和 -PerformMaintenance 新增至 'Set-AzureRmVmss' 和 'Set-AzureRmVmssVM'</span><span class="sxs-lookup"><span data-stu-id="21ce8-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="21ce8-131">將 DisableVMAgent 切換參數新增至 'Set-AzureRmVMOperatingSystem' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="21ce8-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="21ce8-132">'New-AzureRmVm' 和 'New-AzureRmVmss' (簡單參數集全) 支援 'Win10' 映像。</span><span class="sxs-lookup"><span data-stu-id="21ce8-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="21ce8-133">已新增 'Repair-AzureRmVmssServiceFabricUpdateDomain' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21ce8-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="21ce8-134">推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-135">如需詳細資料，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="21ce8-136">'Set-AzureRmVmDiskEncryptionExtension' 讓 AAD 參數成為選用</span><span class="sxs-lookup"><span data-stu-id="21ce8-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="21ce8-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="21ce8-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="21ce8-138">從 Cmdlet 移除取代的 'Tags' 別名</span><span class="sxs-lookup"><span data-stu-id="21ce8-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="21ce8-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="21ce8-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="21ce8-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="21ce8-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="21ce8-141">已將 ADF .Net SDK 更新為版本 0.7.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="21ce8-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="21ce8-142">已在 ExecuteSSISPackage 活動上新增執行參數和連線管理員屬性</span><span class="sxs-lookup"><span data-stu-id="21ce8-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="21ce8-143">已更新 PostgreSql、MySql 連結服務，以使用完整的連接字串，而不是伺服器、資料庫、結構描述、使用者名稱和密碼</span><span class="sxs-lookup"><span data-stu-id="21ce8-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="21ce8-144">已從 DB2 連結服務中移除結構描述</span><span class="sxs-lookup"><span data-stu-id="21ce8-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="21ce8-145">已從 Teradata 連結服務中移除結構描述屬性</span><span class="sxs-lookup"><span data-stu-id="21ce8-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="21ce8-146">已新增 Responsys 的 LinkedService、Dataset、CopySource</span><span class="sxs-lookup"><span data-stu-id="21ce8-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="21ce8-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="21ce8-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="21ce8-148">從 Cmdlet 移除取代的 'Tags' 別名</span><span class="sxs-lookup"><span data-stu-id="21ce8-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="21ce8-149">'New-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="21ce8-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="21ce8-150">'Set-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="21ce8-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="21ce8-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="21ce8-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="21ce8-152">對 Remove-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl 的遞迴 Acl 變更新增新的功能</span><span class="sxs-lookup"><span data-stu-id="21ce8-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="21ce8-153">新增 Cmdlet 以擷取目錄下的內容摘要</span><span class="sxs-lookup"><span data-stu-id="21ce8-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="21ce8-154">新增 Cmdlet 以擷取磁碟使用量和 ACL 傾印</span><span class="sxs-lookup"><span data-stu-id="21ce8-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="21ce8-155">將 Set-AzureRmDataLakeStoreItemAcl 布林的傳回類型更正為 IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="21ce8-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="21ce8-156">將 Set-AzureRmDataLakeStoreItemAclEntry 布林的傳回類型更正為 IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="21ce8-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="21ce8-157">Export-AzureRmDataLakeStoreItem、Import-AzureRmDataLakeStoreItem、Remove-AzureRmDataLakeStoreItem 的重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="21ce8-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="21ce8-158">AzureRM.Dns</span></span>
* <span data-ttu-id="21ce8-159">推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-160">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="21ce8-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="21ce8-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="21ce8-162">更新 Cmdlet 的說明，加上遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="21ce8-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="21ce8-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="21ce8-163">AzureRM.Insights</span></span>
* <span data-ttu-id="21ce8-164">已推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-165">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="21ce8-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="21ce8-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="21ce8-167">啟用 IotHub 的標記和基本 SKU</span><span class="sxs-lookup"><span data-stu-id="21ce8-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="21ce8-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="21ce8-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="21ce8-169">支援管線案例的重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="21ce8-170">新增新的 Cmdlet：Backup/Restore-AzureKeyVaultManagedStorageAccount、Backup/Restore-AzureKeyVaultCertificate、Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval 和 Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="21ce8-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="21ce8-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="21ce8-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="21ce8-172">從 Cmdlet 移除取代的 'Tags' 別名</span><span class="sxs-lookup"><span data-stu-id="21ce8-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="21ce8-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="21ce8-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="21ce8-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="21ce8-174">AzureRM.Media</span></span>
* <span data-ttu-id="21ce8-175">從 Cmdlet 移除取代的 'Tags' 別名</span><span class="sxs-lookup"><span data-stu-id="21ce8-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="21ce8-176">'Set-AzureRmMediaService'</span><span class="sxs-lookup"><span data-stu-id="21ce8-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="21ce8-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="21ce8-177">AzureRM.Network</span></span>
* <span data-ttu-id="21ce8-178">針對 DDoS 保護計劃資源新增支援</span><span class="sxs-lookup"><span data-stu-id="21ce8-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="21ce8-179">已推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-180">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="21ce8-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="21ce8-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="21ce8-182">推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-183">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="21ce8-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="21ce8-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="21ce8-185">推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-186">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="21ce8-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="21ce8-187">AzureRM.Profile</span></span>
* <span data-ttu-id="21ce8-188">依預設啟用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="21ce8-188">Enable context autosave by default</span></span>
* <span data-ttu-id="21ce8-189">將 USGovernmentOperationalInsightsEndpoint 和 USGovernmentOperationalInsightsEndpointResourceId 屬性新增至適用於 US Gov 的 Azure 環境中。</span><span class="sxs-lookup"><span data-stu-id="21ce8-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="21ce8-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="21ce8-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="21ce8-191">已修正 SiteRecovery 案例中的驗證標頭</span><span class="sxs-lookup"><span data-stu-id="21ce8-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="21ce8-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="21ce8-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="21ce8-193">已推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-194">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="21ce8-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="21ce8-195">AzureRM.Resources</span></span>
* <span data-ttu-id="21ce8-196">從 Get-AzureRmRoledefinition 呼叫中移除已淘汰的參數 -AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="21ce8-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="21ce8-197">在 Get-AzureRmRoleAssignment 結果中納入指派給已刪除的使用者/群組/服務主體</span><span class="sxs-lookup"><span data-stu-id="21ce8-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="21ce8-198">針對範圍和資源類型新增 Tab 完成器</span><span class="sxs-lookup"><span data-stu-id="21ce8-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="21ce8-199">新增用於建立服務主體的便利 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="21ce8-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="21ce8-200">合併 Get-AzureRmResource 的 Get- 和 Find- 功能</span><span class="sxs-lookup"><span data-stu-id="21ce8-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="21ce8-201">新增 AD Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="21ce8-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="21ce8-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="21ce8-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="21ce8-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="21ce8-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="21ce8-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="21ce8-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="21ce8-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="21ce8-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="21ce8-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="21ce8-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="21ce8-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="21ce8-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="21ce8-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21ce8-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="21ce8-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="21ce8-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="21ce8-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="21ce8-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="21ce8-211">更新預設的 Linux 映像版本 SKU</span><span class="sxs-lookup"><span data-stu-id="21ce8-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="21ce8-212">NewAzureServiceFabricCluster.cs 預設 UbuntuServer1604 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="21ce8-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="21ce8-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="21ce8-213">AzureRM.Storage</span></span>
* <span data-ttu-id="21ce8-214">已推出多項重大變更</span><span class="sxs-lookup"><span data-stu-id="21ce8-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="21ce8-215">如需詳細資訊，請參閱移轉指南</span><span class="sxs-lookup"><span data-stu-id="21ce8-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="21ce8-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="21ce8-216">AzureRM.Websites</span></span>
* <span data-ttu-id="21ce8-217">升級至最新版本的網站 SDK</span><span class="sxs-lookup"><span data-stu-id="21ce8-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="21ce8-218">已新增 Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot 的 -AssignIdentity 和 -Httpsonly 屬性</span><span class="sxs-lookup"><span data-stu-id="21ce8-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="21ce8-219">已新增兩個新的 Cmdlet：Get-AzureRmWebAppSnapshots 和 Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="21ce8-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
