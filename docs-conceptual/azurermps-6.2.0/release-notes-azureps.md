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
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853452"
---
# <a name="release-notes"></a><span data-ttu-id="1880c-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="1880c-103">Release notes</span></span>

<span data-ttu-id="1880c-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="1880c-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="1880c-105">6.2.0 - 2018 年 6 月</span><span class="sxs-lookup"><span data-stu-id="1880c-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1880c-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1880c-106">AzureRM.Profile</span></span>
* <span data-ttu-id="1880c-107">修正問題：Newtonsoft.Json 10.0.3 版未在模組匯入時載入</span><span class="sxs-lookup"><span data-stu-id="1880c-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="1880c-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1880c-108">AzureRM.Compute</span></span>
* <span data-ttu-id="1880c-109">VMSS VM 更新功能</span><span class="sxs-lookup"><span data-stu-id="1880c-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="1880c-110">新增 'Update-AzureRmVmssVM' 和 'New-AzureRmVMDataDisk' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1880c-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="1880c-111">將 VirtualMachineScaleSetVM 參數新增至 'Add-AzureRmVMDataDisk' Cmdlet，以支援將資料磁碟新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="1880c-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="1880c-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1880c-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="1880c-113">已將 ADF .Net SDK 更新為版本 0.8.0-preview，包含以下變更：</span><span class="sxs-lookup"><span data-stu-id="1880c-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="1880c-114">新增設定中心存放庫的作業</span><span class="sxs-lookup"><span data-stu-id="1880c-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="1880c-115">將 QuickBooks LinkedService 更新為公開 consumerKey 和 consumerSecret 屬性</span><span class="sxs-lookup"><span data-stu-id="1880c-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="1880c-116">更新從 SecretBase 到 Object 的數個模型類型</span><span class="sxs-lookup"><span data-stu-id="1880c-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="1880c-117">新增 Blob 事件觸發程序</span><span class="sxs-lookup"><span data-stu-id="1880c-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="1880c-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1880c-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="1880c-119">更新文件和範例輸出</span><span class="sxs-lookup"><span data-stu-id="1880c-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="1880c-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1880c-120">AzureRM.Network</span></span>
* <span data-ttu-id="1880c-121">啟用網路監看員 Cmdlet 上的流量分析參數</span><span class="sxs-lookup"><span data-stu-id="1880c-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="1880c-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1880c-122">AzureRM.Resources</span></span>
* <span data-ttu-id="1880c-123">針對從 'Get-AzureRmResource' 傳回的 'PSResource' 物件，修正其中的 'Properties' 屬性問題</span><span class="sxs-lookup"><span data-stu-id="1880c-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="1880c-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="1880c-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="1880c-125">修正更新 ServiceBusQueueJob 時沒有設定新驗證值的問題</span><span class="sxs-lookup"><span data-stu-id="1880c-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="1880c-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1880c-126">AzureRM.Sql</span></span>
* <span data-ttu-id="1880c-127">透過選擇性 LicenseType 參數更新下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1880c-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="1880c-128">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1880c-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="1880c-129">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1880c-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="1880c-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="1880c-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="1880c-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1880c-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="1880c-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1880c-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="1880c-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="1880c-133">AzureRM.Websites</span></span>
* <span data-ttu-id="1880c-134">更新 'New-AzureRMWebApp' 以使用來自策略程式庫的常見演算法。</span><span class="sxs-lookup"><span data-stu-id="1880c-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="1880c-135">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="1880c-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="1880c-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="1880c-136">AzureRM.Profile</span></span>
* <span data-ttu-id="1880c-137">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="1880c-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="1880c-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="1880c-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="1880c-139">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="1880c-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="1880c-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1880c-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="1880c-141">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="1880c-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="1880c-142">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="1880c-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="1880c-143">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="1880c-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="1880c-144">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="1880c-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="1880c-145">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="1880c-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="1880c-146">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="1880c-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="1880c-147">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="1880c-147">Added support for MSI identity</span></span>
* <span data-ttu-id="1880c-148">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="1880c-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="1880c-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="1880c-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="1880c-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="1880c-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="1880c-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="1880c-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="1880c-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="1880c-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="1880c-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="1880c-153">AzureRM.Batch</span></span>
* <span data-ttu-id="1880c-154">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="1880c-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="1880c-155">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="1880c-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="1880c-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="1880c-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="1880c-157">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="1880c-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="1880c-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1880c-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="1880c-159">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="1880c-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="1880c-160">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="1880c-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="1880c-161">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="1880c-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="1880c-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1880c-162">AzureRM.Network</span></span>
* <span data-ttu-id="1880c-163">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="1880c-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="1880c-164">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="1880c-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="1880c-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1880c-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="1880c-166">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="1880c-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="1880c-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1880c-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="1880c-168">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="1880c-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="1880c-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1880c-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="1880c-170">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="1880c-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="1880c-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="1880c-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="1880c-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1880c-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="1880c-173">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="1880c-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="1880c-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="1880c-174">AzureRM.Sql</span></span>
* <span data-ttu-id="1880c-175">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="1880c-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="1880c-176">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="1880c-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="1880c-177">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="1880c-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="1880c-178">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="1880c-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="1880c-179">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="1880c-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="1880c-180">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1880c-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="1880c-181">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1880c-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="1880c-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="1880c-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="1880c-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1880c-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="1880c-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1880c-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="1880c-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1880c-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="1880c-186">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="1880c-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>