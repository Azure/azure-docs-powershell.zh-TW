---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/23/2018
ms.locfileid: "34461679"
---
# <a name="release-notes"></a><span data-ttu-id="6a3a3-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="6a3a3-103">Release notes</span></span>

<span data-ttu-id="6a3a3-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="6a3a3-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="6a3a3-105">6.1.0 - 2018 年 5 月</span><span class="sxs-lookup"><span data-stu-id="6a3a3-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="6a3a3-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a3a3-106">AzureRM.Profile</span></span>
* <span data-ttu-id="6a3a3-107">修正執行 'Clear-AzureRmContext' 會讓空白內容保留先前的預設內容名稱，導致使用者無法以舊名稱建立新內容的問題</span><span class="sxs-lookup"><span data-stu-id="6a3a3-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="6a3a3-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6a3a3-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="6a3a3-109">啟用 AS 上的閘道建立關聯/取消關聯作業。</span><span class="sxs-lookup"><span data-stu-id="6a3a3-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="6a3a3-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a3a3-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="6a3a3-111">已新增 ApiVersions、ApiReleases 和 ApiRevisions 支援</span><span class="sxs-lookup"><span data-stu-id="6a3a3-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="6a3a3-112">已新增 ServiceFabric 後端支援</span><span class="sxs-lookup"><span data-stu-id="6a3a3-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="6a3a3-113">已新增 Application Insights 記錄器支援</span><span class="sxs-lookup"><span data-stu-id="6a3a3-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="6a3a3-114">已新增將 'Basic' sku 辨識為有效 sku 的 API 管理服務支援</span><span class="sxs-lookup"><span data-stu-id="6a3a3-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="6a3a3-115">已針對安裝由私人 CA 發出的憑證做為根或 CA 新增支援</span><span class="sxs-lookup"><span data-stu-id="6a3a3-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="6a3a3-116">已針對透過 KeyVault 和多個 Proxy 主機名稱接受自訂 SSL 憑證新增支援</span><span class="sxs-lookup"><span data-stu-id="6a3a3-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="6a3a3-117">已新增 MSI 身分識別支援</span><span class="sxs-lookup"><span data-stu-id="6a3a3-117">Added support for MSI identity</span></span>
* <span data-ttu-id="6a3a3-118">已新增透過 URL 接受原則的支援 附註：下列 Cmdlet 會在未來的版本中淘汰</span><span class="sxs-lookup"><span data-stu-id="6a3a3-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="6a3a3-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="6a3a3-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="6a3a3-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a3a3-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="6a3a3-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="6a3a3-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="6a3a3-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6a3a3-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="6a3a3-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="6a3a3-123">AzureRM.Batch</span></span>
* <span data-ttu-id="6a3a3-124">發行新的 Cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="6a3a3-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="6a3a3-125">發行新的 Cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="6a3a3-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="6a3a3-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="6a3a3-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="6a3a3-127">在 Cmdlet Get-AzureRmConsumptionUsageDetail 上新增新參數 Expand、ResourceGroup、InstanceName、InstanceId、Tags 和 Top</span><span class="sxs-lookup"><span data-stu-id="6a3a3-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="6a3a3-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6a3a3-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="6a3a3-129">針對 Export-AzureRmDataLakeStoreChildItemProperties 修正範例</span><span class="sxs-lookup"><span data-stu-id="6a3a3-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="6a3a3-130">修正 Set-AzureRmDataLakeStoreItemAclEntry 中 Recurse 案例的 Null 參數例外狀況</span><span class="sxs-lookup"><span data-stu-id="6a3a3-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="6a3a3-131">修正 Set-AzureRmDataLakeStoreItemAclEntry、Set-AzureRmDataLakeStoreItemAcl、Remove-AzureRmDataLakeStoreItemAclEntry 的說明檔</span><span class="sxs-lookup"><span data-stu-id="6a3a3-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="6a3a3-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="6a3a3-132">AzureRM.Network</span></span>
* <span data-ttu-id="6a3a3-133">將網路 SDK 版本從 18.0.0-預覽提高到 19.0.0-預覽</span><span class="sxs-lookup"><span data-stu-id="6a3a3-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="6a3a3-134">新增 Cmdlet 來建立通訊協定設定</span><span class="sxs-lookup"><span data-stu-id="6a3a3-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="6a3a3-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a3a3-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="6a3a3-136">新增 Cmdlet 以將新線路連線新增至現有的快速路由線路。</span><span class="sxs-lookup"><span data-stu-id="6a3a3-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="6a3a3-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a3a3-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6a3a3-138">新增 Cmdlet 以將線路連線從現有的快速路由線路移除。</span><span class="sxs-lookup"><span data-stu-id="6a3a3-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="6a3a3-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a3a3-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="6a3a3-140">新增 Cmdlet 來擷取線路連線</span><span class="sxs-lookup"><span data-stu-id="6a3a3-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="6a3a3-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="6a3a3-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="6a3a3-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a3a3-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="6a3a3-143">固定的伺服器驗證使用方式與產生的憑證 (問題 #5998)</span><span class="sxs-lookup"><span data-stu-id="6a3a3-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="6a3a3-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="6a3a3-144">AzureRM.Sql</span></span>
* <span data-ttu-id="6a3a3-145">已更新稽核 Cmdlet 以允許移除 AuditActions 或 AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="6a3a3-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="6a3a3-146">已修正 Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy 在設定新的彈性保留原則時，命令會失敗的問題；錯誤為：使用 azure 復原服務保存庫設定長期保留原則，且不再支援原則。</span><span class="sxs-lookup"><span data-stu-id="6a3a3-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="6a3a3-147">請提交具有新彈性保留原則的要求。</span><span class="sxs-lookup"><span data-stu-id="6a3a3-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="6a3a3-148">更新所有 Azure Sql Database/ElasticPool 建立/更新相關的 Cmdlet 以使用新的資料庫 API，其可支援縮放和階層相關屬性的 Sku 屬性。</span><span class="sxs-lookup"><span data-stu-id="6a3a3-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="6a3a3-149">更新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6a3a3-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="6a3a3-150">New-AzureRmSqlDatabase；Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a3a3-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="6a3a3-151">New-AzureRmSqlElasticPool；Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6a3a3-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="6a3a3-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="6a3a3-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="6a3a3-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6a3a3-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="6a3a3-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a3a3-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="6a3a3-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6a3a3-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="6a3a3-156">更新 'Get-AzureRmTrafficManagerProfile' 的參數，以便在使用 -Name 參數時需要 -ResourceGroupName 參數。</span><span class="sxs-lookup"><span data-stu-id="6a3a3-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>